FROM ubuntu:bionic

# Install necessary dependencies
RUN apt update && \
	apt install -y \
	build-essential \
	curl \
	python \
	apt-transport-https \
	ca-certificates \
	libssl-dev \
	wget \
	git \
	gcc-arm-linux-gnueabihf \
	g++-arm-linux-gnueabihf

# Set the cross compilation toolchain (armhfv7)
ENV CC=arm-linux-gnueabihf-gcc
ENV CXX=arm-linux-gnueabihf-g++
ENV CC_host="gcc -m32"
ENV CXX_host="g++ -m32"

WORKDIR /workdir

RUN mkdir -p /workdir/proj

ENTRYPOINT [ "/bin/bash" ]