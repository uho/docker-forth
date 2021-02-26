FROM debian:buster 
RUN mkdir /src
VOLUME /src
WORKDIR /src
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
  apt-get install -qy wget qemu-user-static \
  && apt-get clean \
  && rm -rf /var/lib/apt
WORKDIR /
RUN wget https://sourceforge.net/projects/mecrisp/files/mecrisp-stellaris-2.5.6.tar.gz/download \
    && tar xf download
WORKDIR /mecrisp-stellaris-2.5.6/linux
CMD ./terminal-qemu
