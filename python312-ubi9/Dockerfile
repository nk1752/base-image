FROM registry.access.redhat.com/ubi9/ubi:latest

RUN echo "******* update *******"
RUN dnf update -y

RUN echo "******* check os version *******"
RUN cat /etc/os-release

RUN dnf list python3.12*

#RUN dnf install -y python3.12.x86_64  python3.12-devel.x86_64 python3.12-pip.noarch python3.12-setuptools.noarch
RUN dnf install -y python3.12  python3.12-devel python3.12-pip

# RUN dnf remove /user/bin/python

RUN ln -s /usr/local/bin/pip3.12 /usr/local/bin/pip
RUN ln -s /usr/local/bin/python3.12 /usr/local/bin/python

RUN ls -l /usr/bin

RUN echo "******* check pip version *******"
RUN pip3.12 --version

RUN echo "******* check python version *******"
RUN python3.12 --version

RUN pip3.12 install --upgrade pip

RUN pip3.12 install requests

