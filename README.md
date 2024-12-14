# RunningApp
Demo Spring MVC application for organized running

The application is dedicated to running clubs and events, while every event belongs to a club.
The data is stored in PostgreSQL database (in a Docker image). Its tables are automatically updated/created if not present, on app startup.

Controller classes are responsible for routes that provide data to app's html pages (via Thymeleaf library) and requests to the database.

This application also uses Spring Security for registering, logging in and out. The users are also persisted in the database, along with their roles (as a separate table modeling many-to-many relationship). Currently, users with all roles can perform actions on clubs and events - insertion, listing, updating and deletion.

**How to use**

Make sure to open Docker desktop

Run the following in terminal:\
docker-compose up\
mvn clean install\
mvn spring-boot:run

The web application is now available at localhost:8080/home.

Created tables can be seen at localhost:8888 with Adminer tool and populated by choosing SQL command option.
