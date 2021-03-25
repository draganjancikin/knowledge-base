# Docker

## Intro to Docker

Docker is built in Linux containers. Run upper level to Linux Kernel.

## How Docker Works

## Commands

```bash
  docker run image_name
  docker run --name image_name
  docker ps
  docker ps -a
  docker run -p5050:80 image_name
  docker run --name="container_name" -p 5050:80 image_name
  docker rm /container_name

# Remove all stopped containers
  docker container prune
```
