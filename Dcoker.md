# What is Docker?
Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime. Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.

# Installation 
https://docs.docker.com/desktop/mac/install/

# Commands
## List out all running containers
```docker
docker ps
```

# Anatomy
## Dockerfile
A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image.

## Docker ignore
The .dockerignore file is very similar to the .gitignore file in that it allows you to specify a list of files or directories that Docker is to ignore during the build process. This can come in really handy in certain instances.

# FAQ
## What is "COPY . ."
"." Simply means current working directory, so it means copy files from current directory to current directory. 
