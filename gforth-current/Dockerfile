FROM debian:bullseye-slim 
RUN mkdir /src
VOLUME /src
WORKDIR /src
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
  apt-get install -qy gforth automake libtool libtool-bin gcc make git \
  && apt-get clean \
  && rm -rf /var/lib/apt
WORKDIR /
RUN git clone https://github.com/forthy42/gforth.git
WORKDIR /gforth
RUN ./autogen.sh && ./configure && make 
WORKDIR /src
ENTRYPOINT ["/gforth/gforth"]
