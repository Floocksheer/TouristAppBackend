# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Spring Boot 3.5.5 application for a tourist app backend using Java 17. The project uses Maven as the build tool and includes Spring Security, Spring Data JPA with MySQL, and validation capabilities.

## Key Technologies

- **Framework**: Spring Boot 3.5.5
- **Java Version**: 17
- **Build Tool**: Maven
- **Database**: MySQL (with Spring Data JPA)
- **Security**: Spring Security
- **Additional**: Lombok for boilerplate reduction, Spring Boot Validation

## Common Commands

### Development
```bash
# Run the application
./mvnw spring-boot:run

# Compile the project
./mvnw compile

# Clean and compile
./mvnw clean compile
```

### Testing
```bash
# Run all tests
./mvnw test

# Run tests with coverage
./mvnw test jacoco:report

# Run a specific test class
./mvnw test -Dtest=TouristAppBackendApplicationTests
```

### Build and Package
```bash
# Create JAR file
./mvnw package

# Clean build
./mvnw clean package

# Skip tests during build
./mvnw package -DskipTests
```

## Project Structure

```
src/
├── main/
│   ├── java/TouristAppBackend/           # Main application code
│   │   └── TouristAppBackendApplication.java  # Spring Boot main class
│   └── resources/
│       ├── application.properties        # Configuration
│       ├── static/                      # Static web resources
│       └── templates/                   # Template files
└── test/
    └── java/TouristAppBackend/          # Test classes
        └── TouristAppBackendApplicationTests.java
```

## Architecture Notes

- **Package Structure**: Single top-level package `TouristAppBackend`
- **Main Class**: `TouristAppBackendApplication.java` - standard Spring Boot application entry point
- **Configuration**: Uses `application.properties` for configuration
- **Database**: Configured for MySQL with JPA entities
- **Security**: Spring Security is included but not yet configured
- **Testing**: Uses JUnit 5 with Spring Boot Test framework

## Development Guidelines

- Use Lombok annotations to reduce boilerplate code
- Follow Spring Boot conventions for package structure and naming
- Database entities should use JPA annotations
- Use Spring Security for authentication and authorization
- Validate input using Spring Validation annotations
- Configuration should be externalized in `application.properties`