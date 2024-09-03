# Spring Boot Greetings Application

## Objective

This project is a simple Spring Boot application that demonstrates the basics of creating and running a Spring Boot application. The application provides a RESTful API endpoint that returns a greeting message.

## Setup and Installation

### Prerequisites
- Java Development Kit (JDK) 11 or later
- Maven or Gradle (for dependency management)
- An IDE with Spring Boot support (e.g., IntelliJ IDEA, Eclipse, or Spring Tool Suite)
- Postman (for API testing) or curl (command-line tool)

### Installation Steps

1. **Install Spring Boot:**
   If you haven't installed Spring Boot yet, you can do so using your preferred package manager or IDE.

2. **Create a New Project:**
   Use the [Spring Initializr](https://start.spring.io/) tool or your IDE to generate a new Spring Boot project with the following settings:
    - **Project:** Maven or Gradle
    - **Language:** Java
    - **Spring Boot Version:** Latest stable version
    - **Dependencies:** Spring Web

3. **Import the Project:**
   Open the generated project in your IDE.

## Understanding the Structure

1. **Project Structure:**
    - `src/main/java`: Contains the Java source files.
    - `src/main/resources`: Contains the application properties files and static resources.

2. **Main Application Class:**
    - Locate the main application class annotated with `@SpringBootApplication`. This class serves as the entry point for your Spring Boot application.

3. **Properties Files:**
    - Check the `application.properties` or `application.yml` file in `src/main/resources` for configuration options.

## Building the Greetings Application

1. **Creating the REST Controller:**
    - Create a new class named `GreetingController` in the appropriate package (e.g., `com.example.demo`).
    - Implement a single endpoint:
        - **GET /greeting:** Returns a greeting message, e.g., "Hello, World!".

   ```java
   package com.example.demo;

   import org.springframework.web.bind.annotation.GetMapping;
   import org.springframework.web.bind.annotation.RestController;

   @RestController
   public class GreetingController {

       @GetMapping("/greeting")
       public String greeting() {
           return "Hello, World!";
       }
   }
