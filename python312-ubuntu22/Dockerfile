FROM ubuntu:22.04

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get update && \
    apt-get install -y --no-install-recommends python3.11 python3-pip

RUN echo "python3.11 installed successfully"
RUN python3 --version