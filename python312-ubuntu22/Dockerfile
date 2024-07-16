FROM ubuntu:22.04

# check ubuntu version
RUN cat /etc/os-release


RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get update && \
    apt-get install -y --no-install-recommends python3.11 python3-pip

RUN ls -l /usr/bin/

#RUN ln -s /usr/bin/python3.10 /usr/bin/python
#RUN ln -s /usr/bin/pip3 /usr/bin/pip

# create synbolic link for ptthon3.10 & pip3.10
#RUN ln -s /usr/bin/python3.10 /usr/bin/py
#RUN update-alternatives --install /usr/bin/pip pip /usr/bin/pip3 1

# <<------------------ remove the existing link and create new link ------------------>>
RUN rm /usr/bin/pip 
RUN ln -s /usr/bin/pip3.10 /usr/bin/pip
RUN ln -s /usr/bin/python3.10 /usr/bin/py

RUN echo "check python version"
RUN py --version

RUN echo "check pip version"
RUN pip --version

RUN which python3.10