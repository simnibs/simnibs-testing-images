############################################
# Docker for testing SimNIBS
# Copyright (c) 2019 Guilherme B Saturnino
############################################

## This docker file is based on the miniconda3 image https://hub.docker.com/r/continuumio/miniconda3
FROM centos:6

ENV PATH /opt/conda/bin:$PATH

RUN yum install -y gcc

RUN curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -o ~/miniconda.sh && \
    /bin/bash ~/miniconda.sh -b -p /opt/conda && \
    rm -f ~/miniconda.sh

CMD ["/bin/bash"]

