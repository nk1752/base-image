FROM ubuntu:22.04 as base

# install curl, wget, and other tools
RUN apt-get update \
    && apt-get install -y \
    curl \
    wget \
    apt-transport-https 
    #lsb-release \
    #gnupg

RUN apt-get install -y openjdk-21-jdk && \
    apt-get install -y maven


# check for arguments
ARG IMAGE_NAME
RUN echo "image name is --> "${IMAGE_NAME}

RUN echo "************** Install .NET SDK **************"
RUN apt-get update && \
    apt-get install dotnet-sdk-8.0 -y --no-install-recommends


LABEL "type"="${IMAGE_NAME}"
LABEL "nadeem"="khalid"