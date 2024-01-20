### Docker
Its a Containerization platform to run application in container within minimum dependency.

### Virtual Machines (VMs):
1. VM is a complete operating system.
2. It takes more disk space compared to containers and Its heavy
3.  Its less portable

### Containers:
1. It package applications in containers, allowing them to be portable to any operating system
2. It takes minimum dependency to run application and Its lightweight 
3. Portable

### Docker Architecture
![docker-architecture](https://user-images.githubusercontent.com/43399466/217507877-212d3a60-143a-4a1d-ab79-4bb615cb4622.png)

### Docker Cmd
To build image:
`docker build -t my_image:latest .`
To run image:
`docker run -d --name my_container nginx`
To show running container:
`docker ps`
To push image:
`docker push myusername/my_image:latest`
To pull image:
`docker pull ubuntu:latest`
To stop container:
`docker stop my_container`
To remove container:
`docker rm my_container`

### Multi stage Build
Create docker images using multiple stages within a single Dockerfile and the final image is so smaller

### Distroless Images
Its a very minimalistic and lightweight docker images that'll only have runtime environment 

### Base images vs Distroless Images
-Base images in Docker contain a minimal operating system with essential components.
-Distroless images is more minimalistic by excluding unnecessary tools and libraries, focusing solely on the application and its dependencies

### Docker Volume 
