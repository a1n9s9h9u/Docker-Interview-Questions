## Docker Interview Questions

#### Docker

Docker is a very popular and powerful open-source containerization platform that is used for building, deploying, and running applications. Docker allows you to decouple the application/software from the underlying infrastructure.

#### Docker Container

A container is a standard unit of software bundled with dependencies so that applications can be deployed fast and reliably b/w different computing platforms.

In simplest terms, docker containers consist of applications and all their dependencies. They share the kernel and system resources with other containers and run as isolated systems in the host operating system. The main aim of docker containers is to get rid of the infrastructure dependency while deploying and running applications. This means that any containerized application can run on any platform irrespective of the infrastructure being used beneath. Technically, they are just the runtime instances of docker images.

#### Docker Images

Docker images are executable packages(bundled with application code & dependencies, software packages, etc.) for the purpose of creating containers. Docker images can be deployed to any docker environment and the containers can be spun up there to run the application.

#### DockerFile

DockerFile is a text file that has all commands which need to be run for building a given image.

![image](https://user-images.githubusercontent.com/97865583/196016923-a5487c5d-3753-408a-8b60-622ef7d9b4d9.png)

#### Docker Compose

Docker Compose is a YAML file consisting of all the details regarding various services, networks, and volumes that are needed for setting up the Docker-based application. So, docker-compose is used for creating multiple containers, host them and establish communication between them. For the purpose of communication amongst the containers, ports are exposed by each and every container.

#### In order to get the status of all the containers, we run the below command:
```docker
docker ps -a
```
The data of a container remains in it until and unless you delete the container.

#### Docker image registry

A Docker image registry, in simple terms, is an area where the docker images are stored. Instead of converting the applications to containers each and every time, a developer can directly use the images stored in the registry.

#### There are three docker components, they are - Docker Client, Docker Host, and Docker Registry.

Docker Client: This component performs “build” and “run” operations for the purpose of opening communication with the docker host.

Docker Host: This component has the main docker daemon and hosts containers and their associated images. The daemon establishes a connection with the docker registry.

Docker Registry: This component stores the docker images. There can be a public registry or a private one. The most famous public registries are Docker Hub and Docker Cloud.

#### Docker Hub

Docker Hub is a public cloud-based registry provided by Docker for storing public images of the containers along with the provision of finding and sharing them. The images can be pushed to Docker Hub through the docker push command.

#### To export a docker image as an archive you have to run the command:
```docker
docker save -o <exported_name>.tar <container-name>
```
A container MUST be in the stopped state before we can remove it.

#### The command used to get all version information of the client and server is the 
```docker
docker version
```
#### Virtualization vs Containerization

Virtualization helps developers to run and host multiple OS on the hardware of a single physical server.

Containerization helps developers to deploy multiple applications using the same operating system on a single virtual machine or server.

#### What does the docker info command do?

The command gets detailed information about Docker installed on the host system. The information can be like what is the number of containers or images and in what state they are running and hardware specifications like total memory allocated, speed of the processor, kernel version, etc.

Docker can run on both Windows and Linux platforms.

#### Can we use JSON instead of YAML while developing docker-compose file in Docker?

Yes! It can be used. In order to run docker-compose with JSON, docker-compose -f docker-compose.json up can be used.

#### Docker container life cycle

The different stages of the docker container from the start of creating it to its end are called the docker container life cycle.  The most important stages are:

Created: This is the state where the container has just been created new but not started yet.

Running: In this state, the container would be running with all its associated processes.

Paused: This state happens when the running container has been paused.

Stopped: This state happens when the running container has been stopped.

Deleted: In this, the container is in a dead state.
