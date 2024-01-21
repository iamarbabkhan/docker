## Creating my first python "hello world!" Docker image and push to Docker Hub
### I have created an Ubuntu EC2 Instance on AWS and i connect it to Mobaxterm using ssh
![Screenshot-2024-01-21-002413.png](https://i.postimg.cc/LXJ6tYBD/Screenshot-2024-01-21-002413.png)
### install Docker on Ec2
* `sudo apt update`
  
![Screenshot-2024-01-21-002446.png](https://i.postimg.cc/TYfj9fFm/Screenshot-2024-01-21-002446.png)
* `sudo apt install docker.io -y`
  
![Screenshot-2024-01-21-002519.png](https://i.postimg.cc/VNnBgvfq/Screenshot-2024-01-21-002519.png)
### Start Docker deamon
* `sudo systemctl status docker`
  
![Screenshot-2024-01-21-002622.png](https://i.postimg.cc/K8gHXZcz/Screenshot-2024-01-21-002622.png)
* `sudo systemctl start docker`

![Screenshot-2024-01-21-002726.png](https://i.postimg.cc/bY5cSYJy/Screenshot-2024-01-21-002726.png)
### Grant sudo permission to ubuntu to run Docker commands
* `sudo usermod -aG docker ubuntu`

![Screenshot-2024-01-21-002826.png](https://i.postimg.cc/gc7VCQMt/Screenshot-2024-01-21-002826.png)
### Logout and login again on ec2
* `logout`

![Screenshot-2024-01-21-005354.png](https://i.postimg.cc/Y9jYvznC/Screenshot-2024-01-21-005354.png)
### Check docker is running
* `docker run hello-world`

![Screenshot-2024-01-21-003248.png](https://i.postimg.cc/K8xb0Qgq/Screenshot-2024-01-21-003248.png)
### Clone repository
* `git clone https://github.com/iamarbabkhan/docker-notes.git`

![Screenshot-2024-01-21-003354.png](https://i.postimg.cc/BbMP7tnt/Screenshot-2024-01-21-003354.png)
### Login to Docker Hub
* `docker login`

![Screenshot-2024-01-21-004218.png](https://i.postimg.cc/d0HKtyVJ/Screenshot-2024-01-21-004218.png)
### Build Docker Image
*  `docker build -t iamarbabkhan/my-first-docker-image:latest .`

![Screenshot-2024-01-21-004450.png](https://i.postimg.cc/mZXfYMYM/Screenshot-2024-01-21-004450.png)
### Check Docker images
*  `docker images`

![Screenshot-2024-01-21-004746.png](https://i.postimg.cc/pXyNqZRx/Screenshot-2024-01-21-004746.png)
### Run Docker Container
* `docker run -it iamarbabkhan/my-first-docker-image:latest`
**the result would be hello world**

![Screenshot-2024-01-21-004701.png](https://i.postimg.cc/pdm4BXHZ/Screenshot-2024-01-21-004701.png)
### Push the Image to DockerHub 
* `docker push iamarbabkhan/my-first-docker-image:latest`

![Screenshot-2024-01-21-004942.png](https://i.postimg.cc/vZ1nvp4y/Screenshot-2024-01-21-004942.png
###  Check Docker image on Docker Hub
![Screenshot-2024-01-21-005057.png](https://i.postimg.cc/g0xKng9S/Screenshot-2024-01-21-005057.png)
![Screenshot-2024-01-21-005153.png](https://i.postimg.cc/yYJ6p9Hq/Screenshot-2024-01-21-005153.png)
