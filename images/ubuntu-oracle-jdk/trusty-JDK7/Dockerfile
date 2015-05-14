# Forked from n3ziniuka5/ubuntu-oracle-jdk:14.04-JDK7, with the only difference
# that it builds from ubuntu:trusty, rather than ubuntu:14.04
# (https://registry.hub.docker.com/u/n3ziniuka5/ubuntu-oracle-jdk/dockerfile/)

FROM ubuntu:trusty
MAINTAINER Olivier Lange "olange@petit-atelier.ch"

RUN echo debconf shared/accepted-oracle-license-v1-1 select true | debconf-set-selections
RUN echo debconf shared/accepted-oracle-license-v1-1 seen true | debconf-set-selections

RUN apt-get update && \
    apt-get install -y --no-install-recommends software-properties-common && \
    add-apt-repository ppa:webupd8team/java && \
    apt-get update && \
    apt-get install -y --no-install-recommends oracle-java7-installer=7u80+7u60arm-0~webupd8~0

# Run the following command to build the image:
#   docker build -t olange/ubuntu-oracle-jdk:trusty-JDK7 .
