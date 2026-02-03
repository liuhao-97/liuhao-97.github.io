# Get the base Ubuntu image from Docker Hub
FROM ubuntu:18.04
# FROM continuumio/anaconda3:latest

LABEL maintainer="jian.weng@ucla.edu"
ENV DEBIAN_FRONTEND=noninteractive 

# Update apps on the base image
RUN apt-get -y update

# Packages
RUN apt-get install -y autoconf automake autotools-dev curl libmpc-dev libmpfr-dev \
                       libgmp-dev gawk build-essential bison flex texinfo gperf    \
                       libtool patchutils bc libqt4-dev python-dev flex bison      \
                       libgoogle-perftools-dev python-six libssl-dev zlib1g-dev    \
                       zip unzip zsh tmux wget git openssh-client vim emacs        \
                       default-jdk default-jre


RUN echo "deb https://dl.bintray.com/sbt/debian /" | tee -a /etc/apt/sources.list.d/sbt.list &&                                  \
    curl -sL "https://keyserver.ubuntu.com/pks/lookup?op=get&search=0x2EE0EA64E40A89B84B2DF73499E82A75642AC823" | apt-key add && \
    apt-get update &&                                                                                                            \
    apt-get install sbt
