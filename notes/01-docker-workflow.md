# Docker Workflow

```bash
Dockerfile -> Docker Image -> Container
```

Once we create a Dockerfile, we can build a Docker Image from it.

## Build a Docker Image

```bash
docker build -t <image-name>:<tag> .
```

- The `-t` flag is used to tag the image.

Once we have a Docker Image, we can create a container from it.

## Create a container

```bash
docker run -it --rm -d -p 8080:80 --name <container-name> <image-name>:<tag>
```

- We can get the image name from the `docker images` command.
- The `-it` flag is used to run the container in interactive mode.
- The `--rm` flag is used to remove the container after it exits.
- The `-d` flag is used to run the container in detached mode.
- The `-p` flag is used to map a port from the container to the host.
- The `--name` flag is used to give a name to the container.

We can also create a container from an existing Docker Image.
