# Learning Trail

## 04.06.2015

* Built a [Redis/Flask App](https://github.com/olange/learning-docker/tree/master/compositions/redis-flask-app) with [Docker Compose](https://docs.docker.com/compose/) (just following the tutorial)

## 21-23.05.2015

* Read [Protecting the Docker daemon Socket with HTTPS](http://docs.docker.com/articles/https/)
* Installed the Docker Engine with LXC on an Ubuntu host + firewall setup
* Read [Managing Data Volumes in containers](http://docs.docker.com/userguide/dockervolumes/) from the documentation
* Played with data volumes, mounting host folders from the host and backuping data
 
## 14.05.2015

* Created a Dockerfile to build an [Ubuntu Trusty with Oracle JDK7](images/ubuntu-oracle-jdk/trusty-JDK7) image -- a mere copy of [n3ziniuka5/ubuntu-oracle-jdk](https://registry.hub.docker.com/u/n3ziniuka5/ubuntu-oracle-jdk/dockerfile/)
* Read [Dockerfile](https://docs.docker.com/reference/builder/) documentation
* Read [Linking containers together](https://docs.docker.com/userguide/dockerlinks/) from the [«Docker User Guide»](https://docs.docker.com/userguide/)

## 13.05.2015

* [Read «Understanding Docker»](https://docs.docker.com/introduction/understanding-docker/)
* Started reading [«Docker User Guide»](https://docs.docker.com/userguide/): [Dockerizing Applications: a "Hello world"](https://docs.docker.com/userguide/dockerizing), [Working with Containers](https://docs.docker.com/userguide/usingdocker), [Working with Docker Images](https://docs.docker.com/userguide/dockerimages)

## 04.05.2015

* [Online Tutorial](https://www.docker.com/tryit/) a 10 min. walkthru basic `search`, `ps`, `inspect`, `images` commands, and `pull`, `run`, `commit` and `push` workflow
* Watched the intro video [What is Docker?](https://youtu.be/ZzQfxoMFH0U) by Solomon Hykes, Docker’s Founder & CTO (7 min.) « […] Docker is a new unit of delivery […] It allows to ship an app with its external libraries; if two apps are needing two conflicting versions of a library from the host, you do not have to worry: both versions of the library will run side by side, each in a container. […] »
* Read about [Docker and Ansible](http://www.ansible.com/docker)

## 01.05.2015 · Getting the generic provider

* Checked-out [Docker Machine's source code](https://github.com/docker/machine) and merged the [PR/406 pull request](https://github.com/docker/machine/pull/406) of the generic provider
* Started the `dev` Docker Machine with `docker-machine start dev`
* Compiled the Docker Machine with PR/406 with `script/build -osarch="darwin/amd64"` -- interestingly, it compiles within a container, instancied from an image containing all executables required to compile the sources, which demonstrates a nice use case of Docker
* Started looking at the generic driver parameters available in the newly compiled `docker-machine` executable, that supports a new `--driver generic` argument

## 30.04.2015 · Understanding Docker Machine

* Watched video [Demo of Docker Machine Beta](https://www.youtube.com/watch?v=ePwmiS7GAxQ) (7:47 min)
* Read the [Docker Machine User Guide](https://docs.docker.com/machine/)
* Installed `docker-machine` with HomeBrew
* Logged into the VM named `dev` installed by Kitematic with `docker-machine ssh dev` (without launching Kitematic)
* Created a new local VM named `test` with `docker-machine create --driver virtualbox test`
* Upgraded the Boot2Docker ISO image of Kitematic to latest version 1.6.0 with `docker-machine upgrade dev`
* Ran a [busybox](https://registry.hub.docker.com/_/busybox/) container with `docker run` on both `dev` and `test` VMs
* Instanciated two [nginx](https://registry.hub.docker.com/_/nginx/) containers with `docker run -d` on both `dev` and `test` VMs
* Read about a [generic provider](https://github.com/docker/machine/pull/406) (Pull request #406), that would allow to «create» a docker engine within a remote dedicated server

## 18.04.2015 · Discovering Docker and its toolchain

* Installed [Kitematic](https://kitematic.com/) on my MacBook and instanciated an [Ubuntu 14.04](https://registry.hub.docker.com/_/ubuntu/) container from the Docker hub; had to upgrade VirtualBox to the current 4.3.26 version, Kitematic would not start with my existing VirtualBox 4.2
* Read [Docker installation instructions for Ubuntu](http://docs.docker.com/installation/ubuntulinux/)
* Read [Orchestrating Docker with Machine, Swarm and Compose](http://blog.docker.com/2015/02/orchestrating-docker-with-machine-swarm-and-compose/), [Announcing Docker Machine](http://blog.docker.com/2015/02/announcing-docker-machine-beta/), [Announcing Docker Compose](http://blog.docker.com/2015/02/announcing-docker-compose/) and [Scaling Docker with Swarm](http://blog.docker.com/2015/02/scaling-docker-with-swarm/), which rose my interest in Docker
* Read [Boycott Docker](http://www.boycottdocker.org) 
