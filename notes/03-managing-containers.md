# Managing Docker Containers

## List Docker Containers

```bash
docker ps
```

## List Docker Containers with sizes

```bash
docker ps --size
```

## Run a Docker Container

```bash
docker run -it --rm -d -p <port>:<port> --name <container-name> <image-name>:<tag>
```

- `-it` flag is used to run the container in interactive mode.
- `--rm` flag is used to remove the container after it exits.
- `-d` flag is used to run the container in detached mode.
- `-p` flag is used to map a port from the container to the host.
- `--name` flag is used to give a name to the container.

## Stop a Docker Container

```bash
docker stop <container-id>
```

## See the stats of a Docker Container

```bash
docker stats

# or

docker stats <container-id>
```
