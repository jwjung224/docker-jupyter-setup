# docker-jupyter-setup
Dockerfile for Anaconda/Jupyter setup

Based on OS X use

1. Download Dockerfile
2. Create a folder to store Dockerfile
3. Open terminal
4. Go to the folder you created
4. Create Docker image by copy and paste (. means current folder) => <br />
    docker build -t name of container .
5. Check if image is created by copy and paste => <br />
    docker images
6. Run container based on Docker image you created => <br />
    docker run --name yourdockername -p 8888:8888 -v "$PWD/notebooks:/opt/notebooks" -d yourdockername
7. Open http://localhost:8888/ from browser
8. Enter "root" for the password in the browser
9. Stop the container when we are done => <br />
    docker rm -f yourdockername
10. Remove (Erase) one Docker image from the local machine => <br />
    docker rmi -f yourdockername <br />
     (Option) Remove all images <br />
     docker rmi $(docker images -a -q)
