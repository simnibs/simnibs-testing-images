############################################
# Docker for building the SimNIBS installer
# Copyright (c) 2019 Guilherme B Saturnino
############################################

FROM centos:7

ENV PATH /opt/conda/bin:$PATH

RUN yum update -y && \
    yum install -y mesa-libGL yum-utils fontconfig freetype freetype-devel fontconfig-devel libXrender libxkbcommon-x11 && \
    yum groupinstall -y development && \
    yum install -y https://centos7.iuscommunity.org/ius-release.rpm && \
    yum install -y python36u python36u-pip python36u-devel



CMD ["/bin/bash"]

