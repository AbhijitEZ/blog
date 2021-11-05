---
title: Docker for absolute beginner
date: "2021-11-05T23:04:03.284Z"
description: "Overview on docker, how it makes the developer life easy."
---

## What docker solves?

Docker help in creating the virtual container on any OS inside our local machine. There are already other alternative
as well like VirtualBox, VMWare and so on but docker surpress all of them. Due to its core customization over OS and functionality.
So important concepts related to Docker are as follow.

### Container

They are the building block of docker, think of it as a virtual box completely isolated from outer where it's job is only to do things it has
been tasked with.

### Images

Images are the blueprint of container. Container are created from images, for eg: an object is created from class where, Image === class.

### Volumes

In docker volumes stores the container data in the local machine in order to save the data even when container service is down, Most usefull
eg is DB data needs to mounted to local machine in order to keep the track of data on container stop.

### Dockerfile

This is the main file which would be used to create a Docker Image. Most of the os | language | services are supported by this file.

### Docker Compose

This docker compose as a controller of many containers. It can be used to connect all the container within same network, get other container
data and so on. Not used much in production

### Inner keywords used in docker

#### Publish Ports

They allow to listen the container port with outside machine `80:8080` where **80** is local-machine port mapped to **8080** of container.
Published ports can be accessible by external containers and services
```docker

-p 80:8080
```

#### Expose
Expose tell the container listens on the stated port during runtime. By default, the EXPOSE instruction does not expose the container’s ports
to be accessible from the host. In other words, it only makes the stated ports available for inter-container interaction.
```docker

EXPOSE 8080
```
