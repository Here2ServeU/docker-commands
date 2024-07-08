#######################################################
# Basic Commands
#######################################################

* docker run <image-name> # Run a container from an image
* docker run -it <image-name> # Run a container from an image in interactive mode 
* docker run -d <image-name> # Run a container from an image in detached mode 

docker run -p 8080:80 <image-name> # Run a container from an image and map the port 80 of the container to the port 8080 of the host

docker run -v /path/on/host:/path/on/container <image-name> # Run a container from an image and mount a volume from the host to the container   

docker pull <image-name> # Pull an image from the registry

docker stop <container-id> # Stop a running container

docker start <container-id> # Start a stopped container

docker restart <container-id> # Restart a running container

docker ps # List all running containers

docker ps -a # List all containers

docker exec -it <container-id> bash # Execute a command in a running container in interactive mode

docker rm <container-id> # Remove a container

docker rmi <image-id> # Remove an image

# Intermediate commands
docker build -t <image-name> . # Build an image from a Dockerfile

docker images # List all images

docker logs <container-id> # Show the logs of a container

docker inspect <container-id> # Show the details of a container

docker inspect <image-id> # Show the details of an image

docker network ls # List all networks

docker network inspect <network-id> # Show the details of a network

docker network create <network-name> # Create a network

docker network connect <network-name> <container-id> # Connect a container to a network

docker network disconnect <network-name> <container-id> # Disconnect a container from a network

docker volume ls # List all volumes

docker volume inspect <volume-name> # Show the details of a volume

docker volume create <volume-name> # Create a volume

docker volume rm <volume-name> # Remove a volume


#######################################################
# Advanced Commands
#######################################################

docker-compose up # Start services defined in a docker-compose.yml file

docker-compose down # Stop services defined in a docker-compose.yml file

docker-compose ps # List all services defined in a docker-compose.yml file

docker-compose logs <service-name> # Show the logs of a service defined in a docker-compose.yml file

docker-compose exec <service-name> bash # Execute a command in a service defined in a docker-compose.yml file in interactive mode

docker-compose build # Build services defined in a docker-compose.yml file

docker-compose pull # Pull services defined in a docker-compose.yml file

# Advanced commands
docker stack deploy -c <compose-file> <stack-name> # Deploy a stack defined in a docker-compose.yml file

docker stack ls # List all stacks

docker stack ps <stack-name> # List all services of a stack

docker stack rm <stack-name> # Remove a stack

docker swarm init # Initialize a swarm

docker swarm join --token <token> <manager-ip> # Join a swarm

docker service ls # List all services

docker service ps <service-name> # List all tasks of a service

docker service logs <service-name> # Show the logs of a service

docker service scale <service-name>=<number-of-replicas> # Scale a service

docker service update --image <new-image> <service-name> # Update the image of a service

docker service rm <service-name> # Remove a service

docker node ls # List all nodes

docker node inspect <node-id> # Show the details of a node

docker node update --availability drain <node-id> # Drain a node

docker node update --availability active <node-id> # Activate a node

docker node rm <node-id> # Remove a node

docker swarm leave # Leave a swarm

docker swarm leave --force # Leave a swarm and force the removal of the node

docker secret create <secret-name> <file> # Create a secret

docker secret ls # List all secrets

docker secret inspect <secret-name> # Show the details of a secret

docker secret rm <secret-name> # Remove a secret

docker config create <config-name> <file> # Create a config

docker config ls # List all configs

docker config inspect <config-name> # Show the details of a config

docker config rm <config-name> # Remove a config

docker plugin install <plugin-name> # Install a plugin

docker plugin ls # List all plugins

docker plugin inspect <plugin-name> # Show the details of a plugin

docker plugin rm <plugin-name> # Remove a plugin

docker system df # Show the disk usage

docker system prune # Remove all stopped containers, all networks not used by at least one container, all dangling images, and all build cache

docker system prune -a # Remove all stopped containers, all networks not used by at least one container, all images, and all build cache

docker system info # Show system-wide information

docker version # Show the Docker version

docker info # Show system-wide information
