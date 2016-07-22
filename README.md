# Udacity Fullstack Item Catalog Learning

This repo contains a web project used for classes leading up to creating the
Item Catalog Project required by the Udacity Full Stack Web Developer
Nanodegree.

I have migrated these files from the Udacity-supplied Vagrant VM to a Docker
container based development environment.

## Creating the Environment

These instructions describe how to build the environment using [Docker for
Mac][1].

### Building an Image to Work from

Check out this repository and then, from the root of the repository, build an
image using the following command:

`docker build -t **tagn** .`

This will create an image from the "official" Python Docker Hub repository,
create a directory to hold the app's files, and install any needed dependencies.

### Running the image

Use the following command to start a container to work in:

`docker run -d -v --rm "$(pwd)":/app -p5000:5000 **tag** python /app/project.py`

This container will link the current directory (the repository root) to the
container and start the app `project.py`. The app will be accessible at the URL:

http://localhost:5000

[1]:https://docs.docker.com/docker-for-mac/
