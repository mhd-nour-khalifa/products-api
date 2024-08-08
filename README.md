# products-api

This project uses [Quarkus](https://quarkus.io/), the Supersonic Subatomic Java Framework.
If you want to learn more about Quarkus, please visit its website: https://quarkus.io/.

## Development Environment Setup

Before running the application, ensure you have the following tools installed:

1. **Java Development Kit (JDK):** [JDK 11 or later](https://adoptium.net/) is required.
2. **Maven:** Download and install from [Maven's official website](https://maven.apache.org/download.cgi).
3. **Docker:** Follow the installation instructions on [Docker's official website](https://docs.docker.com/get-docker/).
4. **PostgreSQL:** Download and install from [PostgreSQL's official website](https://www.postgresql.org/download/).

## Running the Application in a Docker Container

To run the application in a Docker container, navigate to the project's root directory and execute:


docker-compose up
This command will start the application and set up the database connection within the container.

## Build the Docker Image
To build the Docker image, choose one of the Dockerfiles located in src/main/docker that suits your needs and follow the instructions in the Dockerfile.

## Running the Application in Dev Mode (Locally)
For development with live coding, use the following command:

bash
Copy code
./mvnw compile quarkus:dev
NOTE: In dev mode, Quarkus provides a Dev UI accessible at http://localhost:8080/q/dev/.

## Testing the Application
To test the application, run the following command:
./mvnw test

## Packaging and Running the Application
The application can be packaged using:

./mvnw package
It produces the quarkus-run.jar file in the target/quarkus-app/ directory. Be aware that it’s not an über-jar as the dependencies are copied into the target/quarkus-app/lib/ directory.

The application is now runnable using java -jar target/quarkus-app/quarkus-run.jar.

If you want to build an über-jar, execute the following command:

./mvnw package -Dquarkus.package.jar.type=uber-jar
The application, packaged as an über-jar, is now runnable using java -jar target/*-runner.jar.


## Creating a native executable
You can create a native executable using:

./mvnw package -Dnative
Or, if you don't have GraalVM installed, you can run the native executable build in a container using:

./mvnw package -Dnative -Dquarkus.native.container-build=true
You can then execute your native executable with: ./target/products-api-1.0.0-SNAPSHOT-runner

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.


## Related Guides

REST resources for Hibernate ORM with Panache (guide): Generate Jakarta REST resources for your Hibernate Panache entities and repositories
REST (guide): A Jakarta REST implementation utilizing build time processing and Vert.x. This extension is not compatible with the quarkus-resteasy extension, or any of the extensions that depend on it.
REST JSON-B (guide): JSON-B serialization support for Quarkus REST. This extension is not compatible with the quarkus-resteasy extension, or any of the extensions that depend on it.
Hibernate Validator (guide): Validate object properties (field, getter) and method parameters for your beans (REST, CDI, Jakarta Persistence)
RESTEasy Classic JSON-B (guide): JSON-B serialization support for RESTEasy Classic
REST Jackson (guide): Jackson serialization support for Quarkus REST. This extension is not compatible with the quarkus-resteasy extension, or any of the extensions that depend on it
Hibernate ORM with Panache (guide): Simplify your persistence code for Hibernate ORM via the active record or the repository pattern
RESTEasy Classic (guide): REST endpoint framework implementing Jakarta REST and more
REST JAXB (guide): JAXB serialization support for Quarkus REST. This extension is not compatible with the quarkus-resteasy extension, or any of the extensions that depend on it.
JDBC Driver - PostgreSQL (guide): Connect to the PostgreSQL database via JDBC

## Provided Code
Hibernate ORM
Create your first JPA entity

Related guide section...

Related Hibernate with Panache section...

REST Data with Panache
Generating Jakarta REST resources with Panache

Related guide section...

REST
Easily start your REST Web Services

Related guide section...

RESTEasy JAX-RS
Easily start your RESTful Web Services

Related guide sectio




