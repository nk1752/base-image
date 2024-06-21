FROM registry.access.redhat.com/ubi9/ubi:latest

RUN echo "******* update *******"
RUN yum update -y

RUN echo "******* check os version *******"
RUN cat /etc/os-release

# check available python versions
RUN echo "******* check available python versions *******"
RUN yum list python3*

RUN echo "******* install python 3.12 *******"
RUN yum install -y python3.12.x86_64 gcc++ python3.12-devel.x86_64 python3.12-libs.x86_64 python3.12-pip.noarch

# Set Python 3.12 as the default version
RUN ln -s /usr/local/bin/python3.12 /usr/local/bin/python

# install pip3.12 and create a symlink to pip3
RUN echo "******* install pip3.12 *******"
RUN python3.12 -m pip install --upgrade pip
RUN ln -s /usr/local/bin/pip3.12 /usr/local/bin/pip3

RUN echo "******* check python version *******"
RUN python --version