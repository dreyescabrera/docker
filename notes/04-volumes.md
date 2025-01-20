# Managing Docker Volumes

A volume is a shared storage space between the host and the container.

- The host is the machine where the Docker Engine is running.
- The container is the Docker image that we are running.

## Use cases

- Persist data between container restarts.
- Share data between containers.
- Share data between containers and the host.
- Update data in the container without restarting the container.

## Assign a directory to a container as a volume

```bash
docker run -it --rm -d -p 8080:80 --name <container-name> -v <host-directory>:<container-directory> <image-name>:<tag>
```

- `-v` flag is used to assign a directory to a container as a volume.
- `<host-directory>` is the directory on the host.
- `<container-directory>` is the directory inside the container.

### Example

```bash
docker run -it --rm -d -p 8080:80 --name linktree -v ./sitio:/usr/share/nginx/html linktree:latest
```

### Define a volume in a Dockerfile

```bash
FROM nginx:latest

# Path: /usr/share/nginx/html

VOLUME ["./wesbite", "/usr/share/nginx/html"]
```
