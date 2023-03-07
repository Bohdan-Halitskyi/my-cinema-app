# Cinema app

***

**Pet project web app, built for Spring and Hibernate practice.
It allows to send HTTP requests and receive JSON objects and provides basic authentication, authorization and SQL DB management.**

***

## Quick navigation

<!-- TOC -->
[Structure](#structure)</br>
[Functionality](#functionality)</br>
[Technologies](#technologies)</br>
[How to install](#how-to-install)</br>
<!-- TOC -->

### Structure

- `java` 
    - `cinema`
        - `config` Spring configuration classes
        - `contoller` Request controller classes
        - `dao` Low level db operations
        - `dto` DTO projections for `model` contains
        - `exception` Custom exception classes
        - `lib` Custom annotations
        - `model` Entity classes
        - `security` Custom security solutions
        - `service` DAO service classes and mappers
        - `util` formatter for date and time
- `resources` db properties container

### Functionality

**It can:**

- **GET:** /cinema-halls - (user/admin) - get a list of all cinema halls.
- **GET:** /movies - (user/admin) - get a list of all movies.
- **GET:** /movie-sessions/available - (user/admin) - returns available movie sessions for specified movie and date.
- **GET:** /orders - (user) - get list of orders for current user.
- **GET:** /shopping-carts/by-user - (user) - get shopping cart of current user.
- **GET:** /users/by-email - (admin) - get user by email.
- **POST:** /register - (all) - register as a new user.
- **POST:** /cinema-halls - (admin) - create a new cinema hall.
- **POST:** /movies - (admin) - create a new movie.
- **POST:** /movie-sessions - (admin) - create movie session.
- **POST:** /orders/complete - (user) - create a new order for current user (transfer movie tickets from shopping cart to order and clear shopping cart).
- **PUT:** /movie-sessions/{id} - (admin) - update movie session.
- **PUT:** /shopping-carts/movie-sessions - (user) - creates a ticket for specified movie session and adds it to shopping cart of current user.
- **DELETE:** /movie-sessions/{id} - (admin) - delete movie session.

### Technologies

- IntelliJ Idea
- Tomcat 9.0.50
- MySQL
- Maven
- JDK 17
- Spring Web MVC + Security
- Hibernate
- Postman

### How to install

Clone this repo &rarr; customize db.properties &rarr; configure Tomcat &rarr; run 