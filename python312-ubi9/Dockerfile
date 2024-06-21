FROM registry.access.redhat.com/ubi9/ubi:latest

RUN echo "******* update *******"
RUN yum update -y

RUN echo "******* check os version *******"
RUN cat /etc/os-release

# check available python versions
RUN echo "******* check available python versions *******"
RUN yum list python3*

RUN echo "******* install python 3.12 *******"
RUN yum install -y python3.12

RUN echo "******* check python version *******"
RUN python3 --version