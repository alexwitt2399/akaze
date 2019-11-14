# Start from cuda/cudnn docker image
FROM alexwitt23/opencv_cuda:4.1.0

WORKDIR /

# Install dependencies
RUN apt-get update \
    && apt-get install -y \
        wget \
	build-essential \
	gcc \
	g++ \
    && rm -rf /var/lib/apt/lists/*
    
# Install Cmake
RUN cd /tmp &&\
    wget https://github.com/Kitware/CMake/releases/download/v3.14.4/cmake-3.14.4-Linux-x86_64.sh &&\
    chmod +x cmake-3.14.4-Linux-x86_64.sh &&\
    ./cmake-3.14.4-Linux-x86_64.sh --prefix=/usr/local --exclude-subdir --skip-license &&\
    rm ./cmake-3.14.4-Linux-x86_64.sh

WORKDIR /host
