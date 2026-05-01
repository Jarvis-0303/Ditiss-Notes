
1.  Install Docker on ubuntu
```
# Add Docker's official GPG key:
sudo apt update
sudo apt install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
sudo tee /etc/apt/sources.list.d/docker.sources <<EOF
Types: deb
URIs: https://download.docker.com/linux/ubuntu
Suites: $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}")
Components: stable
Architectures: $(dpkg --print-architecture)
Signed-By: /etc/apt/keyrings/docker.asc
EOF

sudo apt update
```
2. 
```
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

3.
 ```
sudo groupadd docker
```
4

```
sudo usermod -aG docker $(whoami)
```
5 
```
sudo reboot
```
6
```
docker ps
```


## Some basic commands
1. Download an image
```
docker images
docker pull ngix:latest
docker images
```

2. start a container form the image
```
docker run --name test -d -o 8080:80 nginx:latest
# in browser localhost:8080
docker ps
```
3. execute a command inside the container
```
docker exec -it test /bin/bash
ls
exit
```
4. Delete the container
```
docker      ps
docker    stop   test
docker    rm   test
docker    ps   -a
```



| Command                                    | Description                                             |
| ------------------------------------------ | ------------------------------------------------------- |
| docker images                              | List all Docker images available on your machine        |
| docker pull nginx:latest                   | Download the latest Nginx image from Docker Hub         |
| docker run ... nginx:latest                | Create and start a container using the Nginx image      |
| docker exec -it <container_name> /bin/bash | Open an interactive terminal inside a running container |
| docker ps                                  | Show all currently running containers                   |
| docker stop test                           | Stop the container named test                           |
| docker rm test                             | Remove the container named test                         |
| docker ps -a                               | Show all containers (running + stopped)                 |





| Step | Task | Command |
| --- | --- | --- |
| 1 | Clone an app from a GitHub repo | cd    ~git   clone   https://github.com/newdelthis/webappdemo.git |
| 2 | Inspect the app’s Dockerfile | cd    webappdemocat   Dockerfile |
| 3 | Containerize the app | docker   build   -t   test:1.0    .docker    images |
| 4 | Run the app as a container | docker   run   -d  --name  web-1  -p  9999:8080  test:1.0In the browser: localhost:9999docker   psdocker   rm    web1    -fdocker    rmi   test:1.0 |


### Docker Image Command
```
dcoker pull image_name
docker images
docker rmiimage_name
```

### Docker Prune Image Command
```
#Img download
docker pull nginx
# Create container
docker run -dit --name t1 nginx
docker stop t1
docker rm t1
docker image
docker image prune -a
```


### Docker Start, Stop and Remove Container

```
docker run container_name
docker container prune
docker stop container_name
```

## How to build our own docker image

1. Write your code in any language eg python, java, cpp etc
   ```
   mkdir ~/hello_python
   vim hello.py
   ```
2. create "Dockerfile' ```Dockerfile``` it contain set of instruction
```
vim Dockerfile
```
in that docker file copy this and change what you need
```
FROM python:3.9
WORKDIR  /app
COPY  hello.py /app
CMD  ["python", "hello.py"]
```
3
```
docker build -t <your_img_name> .
```
4
```
docker run <your _image_name>
```

### Push to Docker

```
docker build -t <docker_UID>/<img_name> :1.0
```
```
docker push <docker_UID>/<img_name> :1.0
```


### To creating JAVA image

```
mkdir ~/hello_java
cd ~/hello_java
```
```
vim Helloworld.java
```
inside Helloworld.java
```
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

```
vim Dockerfile
```
inside dockerfile
```
FROM  eclipse-ter
WORKDIR  /app
COPY  Helloworld.java /app
RUN  javac HElloworld.java
CMD  ["java", "Helloworld.java"]
```
```
docker build -t docker_uid/cdac-java :1.0
```
```
docker run docker_uid/cdac-java :1.0
```


