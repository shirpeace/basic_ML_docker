FROM ubuntu:20.04

ARG user_name="shir"
ARG workspace_dir=/home/${user_name}/workspace_dir

# Disable interactive mode
ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install --no-install-recommends -y \
    git \
    python3-pip \
    python-is-python3 \
    libgl1-mesa-glx \
    python3-tk \ 
    libglib2.0-0 \
    python3-dev \ 
    build-essential \
    xorg-dev \
    libglu1-mesa-dev \
    cmake \
    openssl \
    curl \
    libssl-dev \
    unzip \
    libxinerama-dev \
    libxcursor-dev \
    libusb-1.0-0-dev \
    wget && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR ${workspace_dir}

COPY .. .

RUN pip install -r docker_utils/requirements.txt
