############################################
# Docker for testing SimNIBS
# Copyright (c) 2019, 2020 Guilherme B Saturnino
############################################

## This docker file is based on the miniconda3 image https://hub.docker.com/r/continuumio/miniconda3
FROM centos:7

ENV PATH /opt/conda/bin:$PATH

# Download stuff for OpenGL, X and gzip
RUN yum update -y && \
    yum install -y mesa-libGL yum-utils fontconfig freetype freetype-devel fontconfig-devel libXrender libxkbcommon-x11 bzip2

# Download gcc 8 compilers
RUN yum install -y centos-release-scl && \
    yum-config-manager --enable rhel-server-rhscl-7-rpms && \
    yum install -y devtoolset-8

# Install miniconda
RUN curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -o ~/miniconda.sh && \
    /bin/bash ~/miniconda.sh -b -p /opt/conda && \
    rm -f ~/miniconda.sh

# Install git
RUN yum install git

RUN echo "source /opt/rh/devtoolset-8/enable" >> /etc/bashrc
SHELL ["/bin/bash", "--login", "-c"]
