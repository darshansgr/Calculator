# Calculator Application

## Description
This is a simple calculator application built using HTML, CSS, and JavaScript. The application is containerized using Docker with the Apache HTTP Server.

## Prerequisites

- Docker installed on your system

## Build the Docker Image

```bash
docker build -t calculator-app .
```

## Run the Docker Container

```bash
docker run -d -p 8080:80 --name calculator calculator-app
```

Open the application in your browser:

```
http://localhost:8080
```

## Run with Bind Mount 

To reflect code changes without rebuilding the image:

```bash
docker run -d -p 8080:80 --name calculator -v "${PWD}:/usr/local/apache2/htdocs" calculator-app
```

## Stop the Container

```bash
docker stop calculator
```

## Remove the Container

```bash
docker rm calculator
```