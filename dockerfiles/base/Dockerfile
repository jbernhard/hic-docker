FROM ubuntu:16.10
MAINTAINER Jonah Bernhard <jonah.bernhard@gmail.com>

RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8

RUN apt-get update && apt-get install --yes --no-install-recommends \
    libgfortran3 \
    libboost-filesystem1.61.0 \
    libboost-program-options1.61.0 \
    libhdf5-cpp-11 \
    python3 \
    python3-h5py \
    python3-numpy \
    python3-scipy \
  && rm -rf /var/lib/apt/lists/*
