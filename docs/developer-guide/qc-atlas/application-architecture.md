# Application Architecture

## Implementation rules/guidelines

The operations we have implemented in the three layers follow the following basic rules.
Some of the criterea listed below are used to build tests, e.g. throwing an Exception if an object is not found.

### Controllers

### Services

Service methods should follow the following guidelines:

- A method, performing write access to the database should be annotated with `@Transactional`
- Services should be separated in an interface describing the methods exposed to the Controllers and other services and an Implementation class that implements the service methods.
- To check if an object exists the `exists` method of a repository shall be used
- If an object does not exist, or an object does not exist in the requested relationship a `NoSuchElementException` shall be thrown
- 

### Repositories

Repository interfaces, for JPA should follow the following guidelines:

- Native queries should be avoided
- Use Method based queries where possible
    - The use of JQL (using the `@Query` annotation) should only be done if mandatory
- Lists should return `Page<T>` objects and take `Pageable`s as a input parameter
- In case of single elements `Optional`s should be used
- To check if something exists a `exists` method, e.g. `existsById`, should be used.