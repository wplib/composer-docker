![Composer 1.6.x](https://img.shields.io/badge/Composer-1.6.x-green.svg)
![Composer 1.5.x](https://img.shields.io/badge/Composer-1.5.x-green.svg)
![Composer 1.4.x](https://img.shields.io/badge/Composer-1.4.x-green.svg)

![WPLib-Box](https://github.com/wplib/wplib.github.io/raw/master/WPLib-Box-100x.png)


# Composer Docker Container for WPLib Box
This is the repository for the [Composer](https://getcomposer.org/) Docker container implemented for [WPLib-Box](https://github.com/wplib/wplib-box).
It currently provides versions 1.4.x 1.5.x 1.6.x


## Supported tags and respective Dockerfiles

`1.6.4`, `1.6`, `latest` _([1.6.4/Dockerfile](https://github.com/wplib/composer-docker/blob/master/1.6.4/Dockerfile))_

`1.5.6`, `1.5` _([1.5.6/Dockerfile](https://github.com/wplib/composer-docker/blob/master/1.5.6/Dockerfile))_

`1.4.3`, `1.4` _([1.4.3/Dockerfile](https://github.com/wplib/composer-docker/blob/master/1.4.3/Dockerfile))_


## Using this container.
If you want to use this container as part of WPLib, then use the Docker Hub method.
Or you can use the GitHub method to build and run the container.


## Using it from Docker Hub

### Links
(Docker Hub repo)[https://hub.docker.com/r/wplib/composer/]

(Docker Cloud repo)[https://cloud.docker.com/swarm/wplib/repository/docker/wplib/composer/]


### Setup from Docker Hub
A simple `docker pull wplib/composer` will pull down the latest version.


### Runtime from Docker Hub
start - Spin up a Docker container with the correct runtime configs.

`docker run -d --name composer-1.6.4 --restart unless-stopped --network wplibbox  --user vagrant:vagrant --volume $PWD:/app wplib/composer:1.6.4`


stop - Stop a Docker container.

`docker stop composer-1.6.4`


run - Run a Docker container in the foreground, (all STDOUT and STDERR will go to console). The Container be removed on termination.

`docker run --rm --name composer-1.6.4 --network wplibbox  --user vagrant:vagrant --volume $PWD:/app wplib/composer:1.6.4`


shell - Run a shell, (/bin/bash), within a Docker container.

`docker run --rm --name composer-1.6.4 -i -t --network wplibbox  --user vagrant:vagrant --volume $PWD:/app wplib/composer:1.6.4 /bin/bash`


rm - Remove the Docker container.

`docker container rm composer-1.6.4`


## Using it from GitHub repo

### Setup from GitHub repo
Simply clone this repository to your local machine

`git clone https://github.com/wplib/composer-docker.git`


### Building from GitHub repo
`make build` - Build Docker images. Build all versions from the base directory or specific versions from each directory.


`make list` - List already built Docker images. List all versions from the base directory or specific versions from each directory.


`make clean` - Remove already built Docker images. Remove all versions from the base directory or specific versions from each directory.


`make push` - Push already built Docker images to Docker Hub, (only for WPLib admins). Push all versions from the base directory or specific versions from each directory.


### Runtime from GitHub repo
When you `cd` into a version directory you can also perform a few more actions.

`make start` - Spin up a Docker container with the correct runtime configs.


`make stop` - Stop a Docker container.


`make run` - Run a Docker container in the foreground, (all STDOUT and STDERR will go to console). The Container be removed on termination.


`make shell` - Run a shell, (/bin/bash), within a Docker container.


`make rm` - Remove the Docker container.


`make test` - Will issue a `stop`, `rm`, `clean`, `build`, `create` and `start` on a Docker container.


