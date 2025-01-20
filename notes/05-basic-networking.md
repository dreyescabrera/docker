# Basic Networking

Networking is the process of connecting two or more devices together.

When working with Docker, we can use networking to connect containers between each other and to the host.

If we don't specify a network, the container will be connected to the default network (bridge).

## Create a network

```bash
docker network create <network-name>
```

## List Docker Networks

```bash
docker network ls
```

## Connect a container to a network

```bash
docker network connect <network-name> <container-name>
```

## Gotchas

- Containers can only be connected to one network at a time.
- Containers can only interact with other containers in the same network.
  - This is a security feature to prevent malicious containers from accessing other containers.
