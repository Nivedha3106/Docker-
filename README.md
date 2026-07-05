### What is Docker?

Docker is an open-source platform that allows developers to package an application along with all its dependencies into a container.

This means the application behaves the same regardless of where it is executed.

Instead of saying:

"It works on my machine."

Docker makes it:

"It works on every machine."

### Why Docker?

Before Docker, applications often failed when moved from one environment to another because of differences like:

- Different operating systems
- Different library versions
- Missing dependencies
- Different runtime environments

Docker solves this problem by packaging everything the application needs into one portable container.

Benefits include:

* Consistent development environment
* Faster deployment
* Easy collaboration
* Better resource utilization
* Isolation between applications
* Easier scaling

### Docker Terminologies

## Container

A container is a running instance of a Docker image which packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. 

Think of it as a lightweight isolated environment where your application runs. 

## Image

A Docker image is a blueprint used to create containers.

## Dockerfile

A Dockerfile is a text file that contains instructions for building a Docker image.

Example instructions include:

Selecting a base image
Copying project files
Installing dependencies
Running commands
Starting the application

## Docker Engine

Docker Engine is the core software that makes Docker work.

It is responsible for:

Building images
Running containers
Managing Docker resources

## Docker Client

The Docker Client is the command-line interface (CLI) that we interact with.

Whenever we run commands like:

docker build
docker run
docker ps

the Docker Client sends these requests to the Docker Engine.

## Docker Daemon

The Docker Daemon (dockerd) runs in the background.

It listens for Docker commands and performs operations like:

Building images
Creating containers
Starting containers
Stopping containers
Managing networks and volumes

## Docker Hub

Docker Hub is Docker's public image repository. It stores thousands of pre-built images.

Instead of creating everything from scratch, we can simply pull existing images.

Example:

docker pull nginx

## Docker Registry

A Docker Registry is a service that stores Docker images.

Examples include:

Docker Hub
GitHub Container Registry
Amazon ECR
Azure Container Registry
Google Artifact Registry

Docker Hub is simply one type of registry.

## Volume

Containers are temporary.

If a container is deleted, its internal data is also removed.

Docker Volumes allow data to persist even after containers are deleted.

They are mainly used for:

Databases
Uploaded files
Persistent storage

## Network

Docker provides networking so containers can communicate with each other.

For example:

Frontend Container
        │
        ▼
Backend Container
        │
        ▼
Database Container

Containers don't need to run on the same machine manually—they can communicate over Docker networks.

## Docker Commands

|        Command        |       Description       |
|:---------------------:|:-----------------------:|
| docker --version      | Check Docker version    |
| docker images         | List available images   |
| docker ps             | List running containers |
| docker ps -a          | List all containers     |
| docker pull #         | Download an image       |
| docker build -t app . | Build an image          |
| docker run #          | Run a container         |
| docker stop           | Stop a container        |
| docker rm             | Remove a container      |
| docker rmi #          | Remove an image         |