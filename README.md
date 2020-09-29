## Description

RESTfull API for BulletinBoard

## About

List of available endpoints:
1) GET /ads/all - view list of all rooms.
      Example: http://localhost:8080/ads/all

2) GET /ads/category/{category_id} - view ads filtered by category.
   Example: http://localhost:8080/ads/category/1
   
   
3) POST /users/create - create new user
   Example: http://localhost:8080/users/create with JSON body:
   
   JSON example:
   {
       "username": "John",
       "password": "Qwerty123"
   }
   
4) POST /ads/create - book the room for specified days.


## Structure / Stack
 * Client 
    * ReactJS or another front-end framework or libs
 * api
    * Java 11
    * Spring Boot 2.3
    * Spring Data JPA
    * Spring Security and JWT
    * Spring Test with Junit
    * MySQL
    * Flyway
    * Mail sender 

## Requirements

1. Java 11, maven must be installed (I've recommended [sdkman](https://sdkman.io/install) for this)
2. Docker and docker-compose(read this [article](https://www.digitalocean.com/community/tutorials/how-to-install-docker-compose-on-ubuntu-18-04-ru) or docker documentation)
3. IDE: recommended Intellij IDEA (if possible , the Ultimate version)

## Installation
1. Clone this project
2. Go to folder ```api```
3. Start database using docker(the command is described below)
4. Start application

## Commands for running app
```
    1. docker-compose up db             - started db instance as daemon thread
    2. docker-compose down db           - stopped db instance
    3. docker exec -it bb-api-db bash   - connect to docker container
    4. mysql -h localhost -p            - connect to mysql console(password =root ) 
```
