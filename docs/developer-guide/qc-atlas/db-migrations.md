# Database migrations

For the production version, using tools such as `spring.jpa.hibernate.ddl-auto=update`
[is not recommended](https://stackoverflow.com/questions/221379).
Instead, database migration tools such as Liquibase or Flyway should be used.
For qc-atlas we have chosen the former.

### Workflow

* Edit your Hibernate mapped classes as needed (add and remove classes and attributes)
* Run `mvn compile && mvn liquibase:diffChangeLog`
* Manually check that the new `changelog/yyyy-MM-dd-hh-mm.xml` does what you expect, edit it if it does not
  (for details on how to do that, see the Changelogs section)
* Run `mvn liquibase:update` to update your target database's schema
  (during development, this is done automatically when starting the backend)
* Repeat

The default database credentials are stored in the root `pom.xml` at `db.url` etc.
You can override these using Maven profiles.

### Changelogs

Liquibase uses a changelog to list all changes, in order, made to your database.
To implement complex changes (for example, migrating data), these changelogs need to be written/updated manually.
The following resources help with that:

* [Changelog format overview](https://docs.liquibase.com/concepts/basic/changelog.html)
* [Grouped changes (changesets)](https://docs.liquibase.com/concepts/basic/changeset.html)
* [Change types](https://docs.liquibase.com/change-types/home.html)

All changelogs are stored in the `org.planqk.atlas.core` module at `src/main/resources/db/changes/`.

### Limitations

* Right now, column type changes are ignored by the automatic diff generation tool
  ([see GH](https://github.com/liquibase/liquibase-hibernate/issues/163)).
  These changes need to be recorded manually.
