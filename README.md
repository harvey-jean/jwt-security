# jwt-security

## Overview
This project is a Spring Boot application that demonstrates JWT (JSON Web Token) based authentication and authorization. It includes endpoints for user registration, authentication, and a secured demo endpoint.

## Technologies Used
- Java
- Spring Boot
- Spring Security
- Maven
- JWT (JSON Web Token)

## Project Structure
- `src/main/java/com/harvey/jwtsecurity/auth/AuthenticationController.java`: Handles user registration and authentication.
- `src/main/java/com/harvey/jwtsecurity/demo/DemoController.java`: A secured endpoint that returns a demo message.
- `src/main/java/com/harvey/jwtsecurity/config/JwtService.java`: Service for generating and validating JWT tokens.

## Endpoints
### AuthenticationController
- `POST /api/v1/auth/register`: Registers a new user.
- `POST /api/v1/auth/authenticate`: Authenticates a user and returns a JWT token.

### DemoController
- `GET /api/v1/demo-controller`: A secured endpoint that returns "Hello World from secured endpoint".

## Running the Application
1. Clone the repository:
   ```sh
   git clone https://github.com/harvey-jean/jwt-security.git
    ```

2. Navigate to the project directory:
   ```sh
   cd jwt-security
   ```
3. Build the project using Maven:
   ```sh
   mvn clean install
   ```
4. Run the application:
   ```sh
   mvn spring-boot:run
   ```
## Usage
1. Register a new user by sending a POST request to /api/v1/auth/register with the user details.
2. Authenticate the user by sending a POST request to /api/v1/auth/authenticate with the user credentials to receive a JWT token.
3. Access the secured endpoint /api/v1/demo-controller by including the JWT token in the Authorization header as a Bearer token.