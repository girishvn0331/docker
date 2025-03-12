# Docker Commands Cheat Sheet

This document provides a quick reference guide for essential Docker commands.

## 1. Basic Docker Commands
```sh
docker version      # Show Docker version
docker info        # Display system-wide information
docker help        # Get help for Docker commands
```

## 2. Working with Containers
```sh
docker ps                 # List running containers
docker ps -a              # List all containers
docker run <image>        # Run a container from an image
docker run -it <image> /bin/bash   # Run a container interactively
docker run -d --name <container_name> <image>   # Run container in detached mode
docker stop <container_id>  # Stop a running container
docker start <container_id> # Start a stopped container
docker restart <container_id>  # Restart a container
docker rm <container_id>  # Remove a container
docker logs <container_id>  # View container logs
docker exec -it <container_id> /bin/bash  # Access container shell
```

## 3. Working with Images
```sh
docker images                 # List all images
docker pull <image>           # Pull an image from Docker Hub
docker build -t <image_name> . # Build an image from a Dockerfile
docker tag <image> <repo>:<tag> # Tag an image
docker push <repo>:<tag>       # Push an image to Docker Hub
docker rmi <image_id>         # Remove an image
docker image prune -a         # Remove unused images
```

## 4. Working with Volumes
```sh
docker volume create <volume_name>  # Create a volume
docker volume ls                    # List volumes
docker volume rm <volume_name>      # Remove a volume
docker run -v <volume_name>:/path/in/container <image>  # Attach a volume
```

## 5. Working with Networks
```sh
docker network ls                 # List networks
docker network create <network_name>  # Create a network
docker network inspect <network_name> # Inspect a network
docker network connect <network_name> <container_name>  # Connect a container to a network
docker network disconnect <network_name> <container_name> # Disconnect a container
```

## 6. Docker Compose
```sh
docker-compose up      # Start services in docker-compose.yml
docker-compose down    # Stop and remove containers
docker-compose ps      # List containers in Docker Compose
```

## 7. Docker System Cleanup
```sh
docker system prune  # Remove all unused containers, networks, and images
docker system df     # Show disk usage by Docker
```

---

### Need More Help?
Check the official [Docker Documentation](https://docs.docker.com/) for detailed guides and best practices.
