# Dockerized xv7

This repository contains a Dockerfile to create a Docker image for running xv7, a fork of the xv6 operating system. xv7 includes swapping and paging support. The Docker image includes all necessary dependencies and tools to build and run xv7 in a containerized environment.

## Getting Started

To build the Docker image, run the following command in the root of the repository:

```bash
docker build -t xv7 .
```

Once the image is built, you can run xv7 in a container:

```bash
docker run -it xv7
```

Upon entering the container, you can use the following commands to build and run xv7:

```bash
make clean
make 
make qemu-nox
```

## Development

If you want to make changes to the xv7 codebase, you can mount your local directory into the Docker container:

```bash
docker run -it -v $(pwd):/xv7 xv7
```

This will allow you to edit the code on your host machine and test it inside the container.