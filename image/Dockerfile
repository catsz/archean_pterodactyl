FROM ubuntu:23.10

RUN apt-get update && apt-get install -y \
                        git \
                        openssl \    
                        libpng16-16 \
                        libharfbuzz-bin 
RUN apt clean 
RUN rm -rf /var/lib/apt/list/*
RUN useradd -m -d /home/container container

USER container
ENV USER=container HOME=/home/container
WORKDIR /home/container

COPY --chown=container:container ./../entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["/usr/bin/tini", "-g", "--"]
CMD ["/entrypoint.sh"]
