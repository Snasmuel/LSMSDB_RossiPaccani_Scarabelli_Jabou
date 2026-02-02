# LSMSDB Project - Click&Go

This repository contains the source code, data, and configuration files for the Click&Go Carpooling platform.

## Repository Structure

* **lsmsdb-project/**: Contains the entire Java Spring Boot source code, including the `pom.xml` file.
* **docker_compose_vms/**: Contains three subdirectories. Each subdirectory holds the `docker-compose.yaml` file required to configure the specific environment for each of the 3 Virtual Machines (VMs).
* **DataSet/**: Contains the JSON, CSV, and .cypher files used to populate the databases.
* **loadDb.sh**: A Bash script used to populate the databases. **Note:** This script clears the databases completely before inserting the new data.

## System Requirements

The system is designed to run on a cluster of 3 Virtual Machines. The software requirements for each machine are:

* **Primary VM (Master):** Docker, Java, MongoDB, Redis, Neo4j.
* **Replica VMs (VM 2 & VM 3):** Docker, MongoDB, Redis.

## Build Instructions

To generate the executable JAR file, navigate to the project directory and run the following command. This will compile the code and skip the unit tests during the build process:

```bash
./mvnw clean package -DskipTests
