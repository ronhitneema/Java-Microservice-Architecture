# Spring Boot Microservices

This repository contains the source code of a microservice project developed by Ronhit Neema. The project is built using Spring Boot and Spring Cloud, and it demonstrates the implementation of a microservices architecture.

## Project Overview

The project consists of multiple services that work together to provide a complete application. Each service focuses on a specific functionality and can be independently developed, deployed, and scaled. The following services are included:

1. **api-gateway**: This service acts as an entry point for the entire system, routing incoming requests to the appropriate microservices.

2. **discovery-server**: The discovery server is responsible for service registration and discovery using Spring Cloud Netflix Eureka.

3. **inventory-service**: This service manages the inventory of products, keeping track of available quantities.

4. **notification-service**: The notification service handles sending notifications to users or other services within the system.

5. **order-service**: This service manages the ordering process, including creating, updating, and canceling orders.

6. **product-service**: The product service handles product-related operations, such as retrieving product information and managing the product catalog.

7. **prometheus**: This directory contains files related to monitoring the microservices using Prometheus and Grafana.

8. **realms**: This directory is a work-in-progress and likely contains code related to user authentication and authorization.

## Getting Started

To run the application, you have two options: using Docker or running the services individually without Docker.

### Running with Docker

1. Make sure you have Docker installed on your machine.

2. Open a terminal or command prompt and navigate to the project's root directory.

3. Run the following command to build the applications and create the Docker images:

mvn clean package -DskipTests

4. Once the build is complete, run the following command to start the applications using Docker:

docker-compose up -d

This command will start all the services defined in the `docker-compose.yml` file.

### Running without Docker

1. Make sure you have Maven installed on your machine.

2. Open a terminal or command prompt and navigate to each service's directory.

3. Run the following command in each service's directory to build the application:

mvn clean verify -DskipTests

4. After the build is successful, run the following command in each service's directory to start the application:

mvn spring-boot:run

Repeat this command for each service.

## Topics

This project covers the following topics:

- Microservices architecture
- Spring Boot
- Spring Cloud

Feel free to explore the source code to learn more about each service and their specific functionalities.