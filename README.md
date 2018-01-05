# docker-info
Python example project to publish information retrieved from docker api

## Introduction

This software project has the intent to learn about how to consume the docker api programatically.

## Goal

The goal of the project is generate two docker container that has the following functions.

Container1: [nginx]

- NGINX based container that server static file called index.html, the container must be created from scratch (do not use a dockerhub one)

Container2: [python]

- Python based container should use Docker Python SDK to query information about the docker API and writes a static file called index.html that is mounted in container one.

The container one should display the following information in the index.html:

- List docker images
- List docker containers
- List docker volumes and networks

The container should publish and rest endpoint that returns in json the following information:

- Current hostname
- Current ip address

The endpoint should be accessible from the [NGINX] container and published as localhost/status

The container1 [NGINX] should load balanced the container2 [Python]. The goal is to have at the least 3 containers2 [Python] (running).

```
Good luck
```
