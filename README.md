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
