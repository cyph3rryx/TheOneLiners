# Docker Installation

This repository contains scripts and instructions for installing Docker Engine, creating a Dockerfile, building a Docker image, and running a Docker container. The provided scripts are designed for Ubuntu 22.04 LTS.

## Scripts

### [1] Installing Docker Engine.sh

This script automates the installation of Docker Engine on Ubuntu 22.04 LTS. It performs the following steps:

- Update package repositories
- Install required dependencies
- Configure Docker repository and GPG key
- Install Docker Engine, CLI, containerd.io, docker-buildx-plugin, and docker-compose-plugin
- Add the user "htb-student" to the Docker group
- Display a reminder to log out and log back in for group changes to take effect
- Test Docker installation with a "hello-world" container

To use the script, run:

```bash
./Docker\ Engine\ Install.sh
```

### [2] Docker File.sh

This script creates a Dockerfile for building a Docker image based on Ubuntu 22.04 LTS. The Dockerfile sets up Apache2 and OpenSSH, creates a user named "docker-user" with a password, and grants the user access to Apache and SSH services.

### [3] Docker Build.sh

This script builds a Docker image using the Dockerfile created in [2]. It tags the image as "FS_docker." To build the Docker image, run:

```bash
./Docker\ Build.sh
```

### [4] Docker Run.sh

This script runs a Docker container based on the previously built image. It maps host ports to container ports and runs the container in detached mode. Modify the script to specify the desired host port, container port, and container name.

```bash
./Docker\ Run.sh
```

## Usage

1. Execute [1] Installing Docker Engine.sh to install Docker Engine.
2. Create a Dockerfile using [2] Docker File.sh.
3. Build a Docker image with [3] Docker Build.sh.
4. Run a Docker container using [4] Docker Run.sh.
