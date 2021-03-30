FROM debian:buster-slim

RUN mkdir /src
VOLUME /src

RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
  apt-get install -qy automake libtool libtool-bin gcc make git \
  && apt-get clean \
  && rm -rf /var/lib/apt

RUN git clone https://github.com/MitchBradley/cforth.git
WORKDIR /cforth/build/host-serial-linux64
RUN make 

ENTRYPOINT ["/cforth/build/host-serial-linux64/forth"]
