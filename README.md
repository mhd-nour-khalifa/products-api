# products-api

This project uses [Quarkus](https://quarkus.io/), the Supersonic Subatomic Java Framework.

## Development Environment Setup

1. **Install Java Development Kit (JDK):** Ensure you have [JDK 11 or later](https://adoptium.net/) installed.
2. **Install Maven:** You can download it from [Maven's official website](https://maven.apache.org/download.cgi).
3. **Install Docker:** Follow the instructions on [Docker's official website](https://docs.docker.com/get-docker/).
4. **Install PostgreSQL:** You can download it from [PostgreSQL's official website](https://www.postgresql.org/download/).

## Running the Application in a Docker Container

To run the application in a Docker container, execute the following command in the project's root directory:

```bash
docker-compose up
Build the Docker Image using the Dockerfile
To build the Docker image, choose any of the three Dockerfiles that suit your needs from the path src/main/docker and follow the instructions provided.

Running the Application in Dev Mode (Locally)
You can run the application in dev mode, which enables live coding, using the command below:

bash
Copy code
./mvnw compile quarkus:dev
NOTE: Quarkus ships with a Dev UI, available only in dev mode at http://localhost:8080/q/dev/.

Testing the Application
To test the application, run the following command:

bash
Copy code
./mvnw test
Packaging and Running the Application
The application can be packaged using:

bash
Copy code
./mvnw package
This produces the quarkus-run.jar file in the target/quarkus-app/ directory. Note that it’s not an über-jar; the dependencies are copied into the target/quarkus-app/lib/ directory.

To run the application:

bash
Copy code
java -jar target/quarkus-app/quarkus-run.jar
Building an Über-Jar
To build an über-jar, execute the following command:

bash
Copy code
./mvnw package -Dquarkus.package.jar.type=uber-jar
The application, packaged as an über-jar, is now runnable using:

bash
Copy code
java -jar target/*-runner.jar
Creating a Native Executable
You can create a native executable using:

bash
Copy code
./mvnw package -Dnative
Or, if you don't have GraalVM installed, you can build the native executable in a container using:

bash
Copy code
./mvnw package -Dnative -Dquarkus.native.container-build=true
To execute the native executable:

bash
Copy code
./target/products-api-1.0.0-SNAPSHOT-runner
For more information on building native executables, please consult the Quarkus guide on Maven tooling.

Related Guides
REST resources for Hibernate ORM with Panache: Generate Jakarta REST resources for your Hibernate Panache entities and repositories.
REST: A Jakarta REST implementation utilizing build time processing and Vert.x.
REST JSON-B: JSON-B serialization support for Quarkus REST.
Hibernate Validator: Validate object properties and method parameters for your beans.
RESTEasy Classic JSON-B: JSON-B serialization support for RESTEasy Classic.
REST Jackson: Jackson serialization support for Quarkus REST.
Hibernate ORM with Panache: Simplify your persistence code for Hibernate ORM.
RESTEasy Classic: REST endpoint framework implementing Jakarta REST.
REST JAXB: JAXB serialization support for Quarkus REST.
JDBC Driver - PostgreSQL: Connect to the PostgreSQL database via JDBC.
Provided Code
Hibernate ORM
Create your first JPA entity.

REST Data with Panache
Generate Jakarta REST resources with Panache.

RESTEasy JAX-RS
Easily start your RESTful Web Services.
