# Managing Docker Images

## List Docker Images

```bash
docker images
```

## Get one Docker Image

```bash
docker image inspect <image-name>:<tag>
```

## Filter Docker Images

```bash
docker image ls --filter=reference=<image-name>:<tag>
```

- Can use wildcards, like `docker image ls --filter=reference=nginx:*`

## See all Docker Images with full IDs

```bash
docker image  --no-trunc
```

## Update a Docker Image

```bash
docker image tag <image-name>:<tag> <image-name>:<new-tag>
```

- New tag can be a version number.

## Remove a Docker Image

```bash
docker rmi <image-name>:<tag>

# or

docker rmi <image-id>
```

- The output will be `Untagged: <image-name>:<tag>`.
- If the image has more than one tag, only the most recent tag will be removed, as if we reverted to the previous tag.
- Some images need to be forcefully removed, like `docker rmi -f <image-id>`. That's because the image is still in use or is referenced in multiple containers.

## To keep investigating later

- Untagged vs. Deleted Images
