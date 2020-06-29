############################################
# Docker for testing SimNIBS
# Copyright (c) 2019 Guilherme B Saturnino
############################################

## This docker file is based on the miniconda3 image https://hub.docker.com/r/continuumio/miniconda3
FROM centos:7

ENV PATH /opt/conda/bin:$PATH

RUN yum update -y && \
    yum install -y mesa-libGL yum-utils fontconfig freetype freetype-devel fontconfig-devel libXrender libxkbcommon-x11 bzip2 gcc

RUN curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -o ~/miniconda.sh && \
    /bin/bash ~/miniconda.sh -b -p /opt/conda && \
    rm -f ~/miniconda.sh

CMD ["/bin/bash"]

