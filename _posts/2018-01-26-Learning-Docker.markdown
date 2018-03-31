---
layout: post
title:  "Learning Docker"
date:   2018-01-26 21:14:30 -0500
categories: Technology
---

# Commonly used docker commands

List all the images

```
docker image ls
```

Start an image as a container

```
docker run -i -t <imageid> /bin/bash
```

# Simple Dockerfile

```
FROM mongo:3.4
EXPOSE 27017
CMD ["--bind_ip", "0.0.0.0"]
ENTRYPOINT [ "mongod" ]
```
Entrypoint is the command that gets executed when the container starts.
CMD has the command arguments.

## Build and create image
```
docker build  -t mymongo .
```

## Run the image
```
docker run -p 127.0.0.1:27017:27017 -v ~/mongodata:/data/db mymongoimg
```
-p 127.0.0.1:27017:27017 : exposes the port to the host OS
-v ~/mongodata:/data/db mymongoimg : Maps a host directory to the container directory, in this example provides a persistant data storage for mongo.
