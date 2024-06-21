FROM registry.access.redhat.com/ubi9/ubi:latest

RUN yum update -y
RUN yum search python3
RUN yum install -y python3
RUN yum install -y python3-pip
RUN yum install -y python3-devel
RUN yum install -y gcc
RUN yum install -y make

RUN pip3 install --upgrade pip

RUN cat /etc/os-release
