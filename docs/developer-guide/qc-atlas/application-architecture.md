# Application Architecture

## Implementation rules/guidelines

The operations we have implemented in the three layers follow the following basic rules.
Some of the criterea listed below are used to build tests, e.g. throwing an Exception if an object is not found.

### General

- Loggers shall be retrieved using the `@Slf4j` class annotation from lombok
- Contructors of Components (Services, Repositories, Controllers...) shall be created using the `@AllArgsConstructor` class annoation
- Attributes of a Component class shall be final


### Controllers

- If a requested resource is not found, the application has to respond with HTTP 404
    - This is mostly done by catching the NoSuchElementException thrown by the services
- Validation is Done using Validation groups and the `@Validated` annotation. There are three:
    - `Create`: Used for requirements in a Dto that must be valid during object creation
    - `Update`: Used for requirements in a Dto that must be valid during object Update
    - `IDOnly`: Used for parts where only an id is needed, like creating a reference, In the commented Dto Class below, one can observe the use of these three classes.
- If the validation fails HTTP 400 is returned including a detailed error message, why the validation failed
- If an object cannot be deleted, e.g. if it is still referenced somewhere, HTTP 404 is returned, usualy by the services throwing an EntityReferenceViolationException.
- Exposed Controller methods should have a meaningful name, to prevent collisions in OpenAPI.
    - For example: `getImplementationsOfAlgorithm` instead of `getImplementations` or `getPublicationsOfImplementation` instead of `getPublications`


#### DTO Validation

```java
@Data
@EqualsAndHashCode
@ToString
@NoArgsConstructor
@Relation(itemRelation = "computeResourceProperty", collectionRelation = "computeResourceProperties")
public class ComputeResourcePropertyDto implements Identifyable {
    // Ensures the ID is not null if the IDOnly class is set as a validation class
    @NotNull(groups = {ValidationGroups.IDOnly.class}, message = "An id is required to perform an update")
    // Ensures an id is not set when during creation
    @Null(groups = {ValidationGroups.Create.class}, message = "The id must be null for creating a compute resource property")
    private UUID id;

    private String value;

    // Naming multiple validation classes ensures these conditions are applied to all applications
    // RequiresID is a custom validator to ensure the child type object contains an ID that is not null
    @RequiresID(groups = {ValidationGroups.Update.class, ValidationGroups.Create.class},
            message = "ComputeResourceProperties must have a type with an ID!")
    @NotNull(groups = {ValidationGroups.Update.class, ValidationGroups.Create.class})
    private ComputeResourcePropertyTypeDto type;
}
```

### Services

Service methods / classes should follow the following guidelines:

- A method, performing write access to the database should be annotated with `@Transactional`
- Services should be separated in an interface describing the methods exposed to the Controllers and other services and an Implementation class that implements the service methods.
- To check if an object exists the `exists` method of a repository shall be used
- If an object does not exist, or an object does not exist in the requested relationship a `NoSuchElementException` shall be thrown
- If an object cannot be deleted, e.g. because it is still referenced by another object a EntityReferenceViolationException should be thrown.
- Exposed methods should have a meaningful name
- Linking two objects like, Implementation and SoftwarePlatform shall be done in the LinkingService


### Repositories

Repository interfaces, for JPA should follow the following guidelines:

- Native queries should be avoided
- Use Method based queries where possible
    - The use of JQL (using the `@Query` annotation) should only be done if mandatory
- Lists should return `Page<T>` objects and take `Pageable`s as a input parameter
- In case of single elements `Optional`s should be used
- To check if something exists a `exists` method, e.g. `existsById`, should be used.

### Database Model Classes

- Sets shall be used as lists where possible to elliminate potential double references
- Lombok shall be used to generate Constructors 