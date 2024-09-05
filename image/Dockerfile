FROM ubuntu:23.10

RUN apt-get update && apt-get install -y 	git 	openssl 	libpng16-16 	libharfbuzz-bin 	&& apt-get clean && rm -rf /var/lib/apt/lists/* && useradd -m -d /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container
CMD ["/bin/bash"]
