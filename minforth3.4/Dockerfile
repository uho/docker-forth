FROM debian:buster 
RUN mkdir /src
VOLUME /src
WORKDIR /src
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
  apt-get install -qy build-essential wget \
  && apt-get clean \
  && rm -rf /var/lib/apt
WORKDIR /
RUN wget https://sourceforge.net/projects/minforth/files/MF348_Linux_211105.tgz
RUN tar xvfz MF348_Linux_211105.tgz
WORKDIR /MF348
RUN cd src && chmod 755 lmake && ./lmake mf2c && ./mf2c && ./lmake mf3
ENTRYPOINT /MF348/src/mf3
