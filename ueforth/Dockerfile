FROM debian:buster 
RUN mkdir /src
VOLUME /src
WORKDIR /src
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
  apt-get install -qy automake libtool libtool-bin gcc make wget bzip2 git nodejs \
  && apt-get clean \
  && rm -rf /var/lib/apt
WORKDIR /
RUN git clone https://github.com/flagxor/eforth.git
WORKDIR /eforth/ueforth
RUN make
WORKDIR /src
ENTRYPOINT ["/eforth/ueforth/out/posix/ueforth"]
