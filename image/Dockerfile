FROM ubuntu:23.10

RUN apt-get update && apt-get install -y 	git 	openssl 	libpng16-16 	libharfbuzz-bin 	&& rm -rf /var/lib/apt/lists/*

RUN useradd -m -d /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container
