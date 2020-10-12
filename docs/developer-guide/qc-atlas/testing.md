# Testing qc-atlas

This document gives an overview on what has been tested in the `qc-atlas` and how the tests in the project may be executed.

## Service (and Repository) Tests

The main goal of the service tests was to check their functionality, to ensure they perform the actions expected.
For example a service test may validate that an Algorithm has been created in the database after calling the corresponding service method to do this
The service tests also verify that a method throws the exceptions expected by the controllers, as defined in the [Application Architecture](application-architecture.md). 

## Controller Tests

The Controller tests test the behaviour of the contollers, especially:

- Exception Behaviour
- Validation
- Response Codes
- Response Format

They completely mock away the services, assuming they behave as defined in [Application Architecture](application-architecture.md).

## Running the Tests

To run all tests a running docker installation on the testing machine is mandatory, in order to execute the Service tests, if this is not present, these tests will be skipped.

To run all the tests just execute:
```bash
mvn clean verify
```

Keep in mind running the tests may take a while, sometimes log output may not even be produced, especially if the images used for database testing have to be
downloaded during the test execution.
