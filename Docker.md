# Docker Theory

- Dockerfile defines what goes on in the environment inside your container.




# Docker Lab

1. [Orientation](https://docs.docker.com/get-started/#recap-and-cheat-sheet)

```
## List Docker CLI commands
docker
docker container --help

## Display Docker version and info
docker --version
docker version
docker info

## Execute Docker image
docker run hello-world

## List Docker images
docker image ls

## List Docker containers (running, all, all in quiet mode)
docker container ls
docker container ls --all
docker container ls -aq

```


2. [Container]()

All codes are listed in [docker-app](docker-app)
```
## first need to create Dockerfile and python codes with requirement.txt

## buid app
docker build -t friendlyhello .  

## run app (2 methods)
docker run -p 4000:80 friendlyhello       // 1. -p mapping your machine’s port 4000 to the container’s published port 80 using -p

docker run -d -p 4000:80 friendlyhello    //2. run app in detach mode
docker container ls
docker container stop $containerId

## share image
docker login
docker tag $image $username/$repository:$tag       //docker tag friendlyhello gordon/get-started:part2
docker image ls
docker push username/repository:tag


## pull and run remote image
docker pull $username/$repository
docker run -p 4000:80 username/repository:tag
```


3. [Services]()



4. [Swarms]()



5. [Stacks]()



6. [Deploy your App]()



## Notes

1. no space on disk for dock

see [answer](https://forums.docker.com/t/no-space-left-on-device-error/10894/17)

```
rm ~/Library/Containers/com.docker.docker/Data/com.docker. driver.amd64-linux/Docker.qcow2
Restart docker
qemu-img resize ~/Library/Containers/com.docker.docker/Data/com.docker. driver.amd64-linux/Docker.qcow2 +10G
```


