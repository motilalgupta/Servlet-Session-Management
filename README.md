# Servlet Session Management

A Java Servlet project demonstrating how to manage user sessions using the `HttpSession` API. This project shows session creation, session tracking, storing user information, retrieving session attributes, and invalidating sessions during logout.

---

## Overview

HTTP is a stateless protocol, meaning each request is processed independently. Session Management allows web applications to maintain user-specific data across multiple requests.

This project demonstrates how Java Servlets use the `HttpSession` interface to manage user sessions and maintain user state throughout the application.

---

## Features

* User Login
* Session Creation
* Store User Information in Session
* Retrieve Session Attributes
* Session Tracking Across Multiple Requests
* Logout Functionality
* Session Invalidation

---

## Technologies Used

* Java
* Servlet API
* Apache Tomcat
* HTML
* Maven

---

## Project Structure

```text
src/
├── LoginServlet.java
├── HomeServlet.java
├── ProfileServlet.java
├── LogoutServlet.java
└── web.xml
```

---

## What is Session Management?

Session Management is a mechanism used to maintain information about a user across multiple HTTP requests.

Since HTTP is stateless, the server cannot remember previous requests from the same user. Sessions help solve this problem by storing user-specific data on the server.

Common use cases:

* User Authentication
* Shopping Cart Management
* User Preferences
* Online Banking Systems
* E-commerce Applications

---

## Session Workflow

1. User submits login credentials.
2. Server creates a new session.
3. User information is stored in the session.
4. Session ID is sent to the client.
5. Client sends the Session ID with subsequent requests.
6. Server retrieves session data whenever required.
7. User logs out and the session is invalidated.

---

## Creating a Session

```java
HttpSession session = request.getSession();
session.setAttribute("username", username);
```

---

## Retrieving Session Data

```java
HttpSession session = request.getSession(false);

if(session != null){
    String username = (String) session.getAttribute("username");
}
```

---

## Invalidating a Session

```java
HttpSession session = request.getSession(false);

if(session != null){
    session.invalidate();
}
```

---

## How to Run

### 1. Clone the Repository

```bash
git clone <repository-url>
```

### 2. Open the Project

Import the project into IntelliJ IDEA or Eclipse.

### 3. Configure Tomcat

Add and configure Apache Tomcat Server.

### 4. Build and Deploy

Build the project and deploy it to the Tomcat server.

### 5. Run the Application

Open your browser and navigate to:

```text
http://localhost:8080/
```

---

## Learning Outcomes

After completing this project, you will understand:

* Stateless Nature of HTTP
* Session Management in Servlets
* Working with HttpSession
* Session Creation and Tracking
* Session Attribute Management
* Session Invalidation
* Login and Logout Flow
* Basic Web Application State Management

---

## Future Improvements

* Database-Based Authentication
* Session Timeout Handling
* Role-Based Authorization
* Remember Me Functionality
* Cookie-Based Session Tracking
* User Registration Module

---

## License

This project is created for learning and educational purposes.

---

## Author

**Motilal Gupta**

Java Developer | Backend Development Enthusiast

Created to learn and demonstrate Session Management using Java Servlets.
