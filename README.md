![Docker Logo](https://www.docker.com/blog/wp-content/uploads/2013/08/KuDr42X_ITXghJhSInDZekNEF0jLt3NeVxtRye3tqco.png)
# Docker Tutorial

## Section 1
[Part 1: Orientation and setup](https://docs.docker.com/get-started/)

### Commands Run
1. `docker --version`
2. `docker run hello-world`
3. `docker image ls`
4. `docker container ls --all`

### What I Learned
`image ls` vs `container ls`
    The image list command shows information about the built binaries, when they were updated and their size.
    The container command shows information about when each container was last created (inaccurate on my system, said "3 hours ago"), its last exit status, assume 0 is success, and time. 
    The container command by default only outputs for running container instances.    


## Section2
[Part 2: Build and run your image](https://docs.docker.com/get-started/part2/)

### Commands Run
1. `git clone https://github.com/dockersamples/node-bulletin-board
    cd node-bulletin-board/bulletin-board-app`
2. `docker image build -t bulletinboard:1.0 .`
3. `docker container run --publish 8000:8080 --detach --name bb bulletinboard:1.0`
4. `docker container rm --force bb`

### What I Learned
There is a general order to the Dockerfile:
 Start with the FROM command to specify an image to base off of. 
Then build up the apps dependencies on the containerized filesystem. 
Finish up by specifying the containers inputs and outputs. 

![App running on :8000](images/Running%20app%20from%20docker%20container.PNG)


## Section 3
[Part 3: Share images on Docker Hub](https://docs.docker.com/get-started/part3/)

### Commands Run
1. `docker image tag bulletinboard:1.0 sgrodberg/bulletinboard:1.0`
2. `docker image push sgrodberg/bulletinboard:1.0`

### What I Learned
* Multiple tags can refer to the same image
* Docker has a repository called Docker Hub where images can be published
* Dockerfile should be under version control

![Published image to docker hub](images/Published%20docker%20image.PNG)
