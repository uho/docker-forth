FROM debian:buster 
RUN mkdir /src
VOLUME /src
WORKDIR /src
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
  apt-get install -qy automake libtool libtool-bin gcc make git \
  && apt-get clean \
  && rm -rf /var/lib/apt
WORKDIR /
RUN git clone https://github.com/nimblemachines/muforth.git
WORKDIR /muforth/src
RUN ./configure.sh && make 
WORKDIR /muforth/mu 
CMD /bin/bash
