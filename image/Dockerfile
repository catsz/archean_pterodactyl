FROM ubuntu:23.10

ARG RELEASE
ARG LAUNCHPAD_BUILD_ARCH
LABEL org.opencontainers.image.ref.name=ubuntu
LABEL org.opencontainers.image.version=23.10

ADD file:492ae1940ef5a9a4d7af92b9120b5b7c7d3bfd8107ce94d28eab844ace024981 in /

RUN apt-get update && apt-get install -y 	git 	openssl 	libpng16-16 	libharfbuzz-bin 	&& rm -rf /var/lib/apt/lists/*

RUN useradd -m -d /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container
