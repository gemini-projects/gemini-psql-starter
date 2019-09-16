
# Gemini Postgresql Starter

This repository can be used to start with Gemini as a Gradle dependency module. You can see more about the framework
 [here](https://github.com/gemini-projects/gemini) or take a look at the [documentation](https://gemini.at7.it/).


## What is included ?

* Custom Gemini Module with some Example Entities and Records
    * *resources/schemas/CUSTOM_MODULE.at*
    * *resources/schemas/CUSTOM_MODULE.atr*
* Simple Gemini Event to add custom logic to fields
    * *../events/EmployeeEvents.java*
* Immutable Domain Entity Configuration Example
* Skeleton to start the development of your APIs

## Build and Run

You can use your favorite IDE. Be sure to use *docker/wd* as working directory if you want to start with provided *application.properties*.

It is Spring App we use common Spring task.

```
# from project root
$ gradle bootJar

# or build an executable
$ gradle executableJar

# copy executable insiede working directory (alraedy crafted with common Spring application.properties)
$ cp dist/gemini-psql-starter-1.0-executable.jar docker/wd/

# start docker services (Database Postgresql, PgAdmin and Swagger to consume APIs)
$ cd docker
$ docker-compose up -d

# once docker services are up
$ cd wd
$ ./gemini-psql-starter-1.0-executable.jar

# now you can use Swagger to consume APIs

```

## License
Apache License 2.0