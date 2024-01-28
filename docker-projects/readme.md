## Creating Python web app Docker image and push to Docker Hub
### I have created an Ubuntu EC2 Instance on AWS and i connect it to Mobaxterm using ssh
### install Docker on Ec2
* `sudo apt update`
* `sudo apt install docker.io -y`
### Start Docker deamon
* `sudo systemctl status docker`
* `sudo systemctl start docker`
### Grant sudo permission to ubuntu to run Docker commands
* `sudo usermod -aG docker ubuntu`
### Check docker is running
* `docker run hello-world`
### Clone repository
* `git clone https://github.com/iamarbabkhan/docker-notes.git`
### Login to Docker Hub
* `docker login`
  
![Screenshot-2024-01-28-023354.png](https://i.postimg.cc/KvVjnpGG/Screenshot-2024-01-28-023354.png)
### Build Docker Image
*  `docker build -t iamarbabkhan/first-django-web-app:latest .`
  
![Screenshot-2024-01-28-030626.png](https://i.postimg.cc/BnkSKjCX/Screenshot-2024-01-28-030626.png)
### Check Docker images
*  `docker images`
  
![Screenshot-2024-01-28-030759.png](https://i.postimg.cc/wx177dzf/Screenshot-2024-01-28-030759.png)
### Run Docker Container
* `docker run -it -p 8000:8000 iamarbabkhan/first-django-web-app:latest`
  
![Screenshot-2024-01-28-030921.png](https://i.postimg.cc/zvvWfLj0/Screenshot-2024-01-28-030921.png)
### Check Docker Container running status
![Screenshot-2024-01-28-031230.png](https://i.postimg.cc/Fs9F05XX/Screenshot-2024-01-28-031230.png)
### Check on web 
![Screenshot-2024-01-28-025735.png](https://i.postimg.cc/DZP0K235/Screenshot-2024-01-28-025735.png)
### Push the Image to DockerHub 
* `docker push iamarbabkhan/first-django-web-app:latest`
  
![Screenshot-2024-01-28-031726.png](https://i.postimg.cc/d01c0wC4/Screenshot-2024-01-28-031726.png)
