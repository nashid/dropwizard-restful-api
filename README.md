# Dropwizard restful API

A shot at building a very simple RESTful, Ruby On Rails-like pure JSON API with DropWizard and JDBI.

## Requirements
- maven
- Java 8

## Configure environment
- Install [sdkman](https://sdkman.io/)
- Commands to list java versions

```
sdk list java
sdk install java 17.0.3-oracle
sdk use java 17.0.3-oracle
```

Now the java version would be set to `17`.

```
java -version
java version "17.0.3" 2022-04-19 LTS
Java(TM) SE Runtime Environment (build 17.0.3+8-LTS-111)
Java HotSpot(TM) 64-Bit Server VM (build 17.0.3+8-LTS-111, mixed mode, sharing)
```
 
## Building the project
`mvn clean package [-DskipTests]`

## Starting the server
`java -jar target/dropwizard-restful-api-1.0-SNAPSHOT.jar server config.yml`

## Example calls
```
GET localhost:8080/contacts
GET localhost:8080/contacts/1
DELETE localhost:8080/contacts/1
POST localhost:8080/contacts
PUT localhost:8080/contacts/1
```
