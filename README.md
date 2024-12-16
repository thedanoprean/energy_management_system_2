# Energy Management System - Advanced Version

## Description
The Energy Management System (EMS) is a comprehensive solution for managing users and their associated smart energy metering devices. It leverages a microservices-based architecture to ensure modularity, scalability, and a seamless user experience.

## Key Features
- **Authentication and Authorization** for users and administrators.
- **CRUD Operations** for user accounts and smart energy metering devices.
- **Role-Based Access Control** to restrict unauthorized access.
- **Data Synchronization** between microservices to ensure consistency.
- **Modular Design** with independent frontend and backend components.

## System Architecture
The EMS consists of the following key components:
1. **Frontend Application**: A React-based interface for interacting with the system.
2. **Microservices**:
   - **User Microservice**: Manages user accounts, authentication, and authorization.
   - **Device Microservice**: Handles smart device registration and management.
   - **Communication Microservice**: Processes energy consumption data from devices.
3. **Databases**: Separate PostgreSQL databases for each microservice to store data.
4. **RabbitMQ**: Facilitates communication between microservices.

### Deployment Overview
The system is containerized using Docker and orchestrated with Docker Compose. Key components include:
- **Frontend**: Exposed on port `7000`, built using Node.js and served with Nginx.
- **User Microservice**: Exposed on port `3000`, developed in Java (Spring Boot).
- **Device Microservice**: Exposed on port `3003`, developed in Java (Spring Boot).
- **Communication Microservice**: Exposed on port `8083`, developed in Java (Spring Boot).
- **PostgreSQL Databases**: Dedicated for users, devices, and communication, with data persistence enabled.

## Functional Requirements
1. **User Management**:
   - User registration, login, update, and deletion.
   - Role-based redirection to administrator or user-specific pages.
2. **Device Management**:
   - Registration, retrieval, update, and deletion of smart energy devices.
   - Association of devices with specific users.
3. **Communication Management**:
   - Processing energy consumption data.
   - Hourly energy usage computation.

## Non-Functional Requirements
- **Performance**: Response time under 1 second for most operations.
- **Scalability**: Supports an increasing number of users and devices.
- **Reliability**: High availability and consistent data synchronization.
- **Usability**: Intuitive frontend with clear error messages.
- **Interoperability**: Seamless communication between microservices via REST APIs.

## Installation and Setup
1. **Prerequisites**:
   - Docker and Docker Compose installed on your machine.
   - Java 17, Node.js, and PostgreSQL installed for local development.

2. **Steps to Run the Application**:
   - Clone the repository: `git clone <repository-url>`
   - Navigate to the project directory: `cd energy-management-system`
   - Build and start containers: `docker-compose up --build`
   - Access the application at `http://localhost:7000`.

3. **Ports Overview**:
   - Frontend: `7000`
   - User Microservice: `3000`
   - Device Microservice: `3003`
   - Communication Microservice: `8083`
   - PostgreSQL Databases: `5404`, `5303`, `5505`

## Future Enhancements
- Real-time monitoring of energy consumption.
- Advanced analytics for energy usage patterns.
- Integration of machine learning for predictive maintenance.

## Conclusion
The EMS is a robust, scalable, and user-friendly solution for energy management. Designed with flexibility and efficiency in mind, it addresses the needs of both administrators and end-users, offering a reliable tool for managing smart energy devices.

## Acknowledgments
- Built with **Java Spring Boot**, **React.js**, **PostgreSQL**, **Docker**, and **RabbitMQ**.
- Inspired by best practices in microservices and energy management.

For detailed documentation, refer to the project's official documentation file.
