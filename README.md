products-api
This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/.

Development Environment Setup
1- Install Java Development Kit (JDK): Ensure you have JDK 11 or later installed.
2- Install maven
3- Install Docker
4- Install PostgreSQL

Running the application in a docker container
to run the application in a docker container, run the following command in the project root dir

docker-compose up
This is crucial to make a successful connection with the database in a container

Build the Docker Image using the Docker File
To build the image choose any of the 3 Dockerfiles that suits you from the path src/main/docker and follow the instructions

Running the application in dev mode (locally)
You can run your application in dev mode that enables live coding using the command below:

./mvnw compile quarkus:dev
NOTE: Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.

Testing the application
To test the application, run the following command:

./mvnw test
Packaging and running the application
The application can be packaged using:

./mvnw package
It produces the quarkus-run.jar file in the target/quarkus-app/ directory. Be aware that it’s not an über-jar as the dependencies are copied into the target/quarkus-app/lib/ directory.

The application is now runnable using java -jar target/quarkus-app/quarkus-run.jar.

If you want to build an über-jar, execute the following command:

./mvnw package -Dquarkus.package.jar.type=uber-jar
The application, packaged as an über-jar, is now runnable using java -jar target/*-runner.jar.

Creating a native executable
You can create a native executable using:

./mvnw package -Dnative
Or, if you don't have GraalVM installed, you can run the native executable build in a container using:

./mvnw package -Dnative -Dquarkus.native.container-build=true
You can then execute your native executable with: ./target/products-api-1.0.0-SNAPSHOT-runner

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.

Related Guides
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
Provided Code
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

Related guide section...
