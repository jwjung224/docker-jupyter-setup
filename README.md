# docker-jupyter-setup
Dockerfile for Anaconda/Jupyter setup

Using it on OS X

1. Download Dockerfile
2. Create folder to store Dockerfile
3. Open terminal
4. Create Docker image by copy and paste (. means current folder) => 
    docker build -t name of container .
5. Check if image is created by copy and paste => 
    docker images
6. Run container based on Docker image we created =>
    docker run --name docker-data-science -p 8888:8888 -v "$PWD/notebooks:/opt/notebooks" -d docker-data-science
7. Open http://localhost:8888/ from browser
8. Enter root for the password in the browser
9. Stop the container when we are done =>
    docker rm -f name of container
10. Remove (Erase) one Docker image from the local machine =>
    docker rmi -f name of container
10.2. (Option) Remove all images
    docker rmi $(docker images -a -q)
