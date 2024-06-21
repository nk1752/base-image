FROM registry.access.redhat.com/ubi9/ubi:latest

# Install dependencies
RUN dnf update -y && \
    dnf install -y curl gcc openssl-devel bzip2-devel libffi-devel make

# check os version
RUN cat /etc/os-release

# Download and extract Python 3.12
RUN curl https://www.python.org/ftp/python/3.12.0/Python-3.12.0.tgz && \
    tar xzf Python-3.12.0.tgz && \
    cd Python-3.12.0 && \
    ./configure --enable-optimizations && \
    make altinstall

# Cleanup
RUN rm -rf Python-3.12.0.tgz Python-3.12.0

# Set Python 3.12 as the default version
RUN ln -s /usr/local/bin/python3.12 /usr/local/bin/python

# Verify installation
RUN python --version

# Add your application code here
