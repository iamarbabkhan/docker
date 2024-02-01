### Start the docker daemon
* `docker -d`
### Docker Image cmd:
1. Build an Image from a Dockerfile
* `docker build -t <image_name>`
2. Build an Image from a Dockerfile without the cache
* `docker build -t <image_name> . –no-cache`
3. List local images
* `docker images`
4. Delete an Image
* `docker rmi <image_name>`
5. Remove all unused images
* `docker image prune`

### Docker Container cmd:
1. Create and run a container from an image, with a custom name:
* `docker run --name <container_name> <image_name>`
2. Run a container with and publish a container’s port(s) to the host.
* `docker run -p <host_port>:<container_port> <image_name>`
3. Run a container in the background
* `docker run -d <image_name>`
4. stop an existing container:
* `docker |stop <container_name> (or <container-id>)`
5. Remove a stopped container:
* `docker rm <container_name>`
6. Open a shell inside a running container:
* `docker exec -it <container_name> sh`
7. Fetch and follow the logs of a container:
* `docker logs -f <container_name>`
8. To inspect a running container:
* `docker inspect <container_name> (or <container_id>)`
9. To list currently running containers:
* `docker ps`
10. List all docker containers (running and stopped):
* `docker ps --all`
11. View resource usage stats
* `docker container stats`
12. run container for limited time
* `docker run -d <image name> sleep 60
Note: it will run for 60 sec and shutdown automatically

### Docker HUB cmd
1. Login into Docker
* `docker login -u <username>`
2. Publish an image to Docker Hub
* `docker push <username>/<image_name>`
3. Search Hub for an image
* `docker search <image_name>`
4. Pull an image from a Docker Hub
* `docker pull <image_name>`
