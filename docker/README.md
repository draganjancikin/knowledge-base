# Docker

## Commands

```bash
# Stops one container.
$ docker stop mycontainer

# Stops all running containers.
$ docker stop $(docker ps -a -q)

# Start all containers.
$ docker start $(docker ps -a -q)

# WARNING! This will remove:
#        - all stopped containers
#        - all networks not used by at least one container
#        - all dangling images
#        - all build cache
$ docker system prune
```