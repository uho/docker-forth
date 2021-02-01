FROM debian:buster 
RUN mkdir /src
VOLUME /src
WORKDIR /src
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
  apt-get install -qy automake libtool libtool-bin gcc make wget bzip2 \
  && apt-get clean \
  && rm -rf /var/lib/apt
WORKDIR /
RUN wget https://sourceforge.net/projects/pfe/files/pfe/0.33.71/pfe-0.33.71.tar.bz2/download \
    && tar xf download
WORKDIR /pfe-0.33.71
RUN sed -i -e 's/,--warn-common//g' pfe/configure \
    && ./configure --prefix=/usr && make && make install
WORKDIR /src
ENTRYPOINT ["/usr/bin/pfe"]
