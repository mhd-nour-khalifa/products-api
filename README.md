# products-api

This project uses [Quarkus](https://quarkus.io/), the Supersonic Subatomic Java Framework.

## Development Environment Setup

Before running the application, ensure you have the following tools installed:

1. **Java Development Kit (JDK):** [JDK 11 or later](https://adoptium.net/) is required.
2. **Maven:** Download and install from [Maven's official website](https://maven.apache.org/download.cgi).
3. **Docker:** Follow the installation instructions on [Docker's official website](https://docs.docker.com/get-docker/).
4. **PostgreSQL:** Download and install from [PostgreSQL's official website](https://www.postgresql.org/download/).

## Running the Application in a Docker Container

To run the application in a Docker container, navigate to the project's root directory and execute:

```bash
docker-compose up
This command will start the application and set up the database connection within the container.

Build the Docker Image
To build the Docker image, choose one of the Dockerfiles located in src/main/docker that suits your needs and follow the instructions in the Dockerfile.

Running the Application in Dev Mode (Locally)
For development with live coding, use the following command:

bash
Copy code
./mvnw compile quarkus:dev
NOTE: In dev mode, Quarkus provides a Dev UI accessible at http://localhost:8080/q/dev/.

Testing the Application
To run tests, execute:

bash
Copy code
./mvnw test
Packaging and Running the Application
To package the application, use:

bash
Copy code
./mvnw package
This creates the quarkus-run.jar file in the target/quarkus-app/ directory. This is not an über-jar; the dependencies are stored in target/quarkus-app/lib/.

To run the packaged application:

bash
Copy code
java -jar target/quarkus-app/quarkus-run.jar
Building an Über-Jar
To create an über-jar, run:

bash
Copy code
./mvnw package -Dquarkus.package.jar.type=uber-jar
You can then run the über-jar with:

bash
Copy code
java -jar target/*-runner.jar
Creating a Native Executable
To build a native executable, use:

bash
Copy code
./mvnw package -Dnative
If GraalVM is not installed, build the native executable within a container:

bash
Copy code
./mvnw package -Dnative -Dquarkus.native.container-build=true
To run the native executable:

bash
Copy code
./target/products-api-1.0.0-SNAPSHOT-runner
For more details on building native executables, refer to the Quarkus guide on Maven tooling.

Related Guides
REST resources for Hibernate ORM with Panache: Generate Jakarta REST resources for Hibernate Panache entities and repositories.
REST: Jakarta REST implementation utilizing build time processing and Vert.x.
REST JSON-B: JSON-B serialization support for Quarkus REST.
Hibernate Validator: Validate object properties and method parameters for your beans.
RESTEasy Classic JSON-B: JSON-B serialization support for RESTEasy Classic.
REST Jackson: Jackson serialization support for Quarkus REST.
Hibernate ORM with Panache: Simplify persistence code for Hibernate ORM.
RESTEasy Classic: REST endpoint framework implementing Jakarta REST.
REST JAXB: JAXB serialization support for Quarkus REST.
JDBC Driver - PostgreSQL: Connect to PostgreSQL database via JDBC.
Provided Code
Hibernate ORM: Create your first JPA entity.
REST Data with Panache: Generate Jakarta REST resources with Panache.
RESTEasy JAX-RS: Easily start your RESTful Web Services.
csharp
Copy code





