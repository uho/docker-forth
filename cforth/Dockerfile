FROM debian:buster as builder

RUN apt update -q \
  && DEBIAN_FRONTEND=noninteractive \
  apt install -qy automake libtool libtool-bin gcc make git \
  && apt clean \
  && rm -rf /var/lib/apt

RUN git clone https://github.com/MitchBradley/cforth.git
WORKDIR /cforth/build/host-serial-linux64
RUN make

RUN tar cvfz /cforth.tgz /cforth

FROM debian:buster-slim

RUN apt update -q && apt upgrade -qy && apt clean && rm -rf /var/lib/apt

RUN mkdir /src
VOLUME /src

COPY --from=builder /cforth.tgz /cforth.tgz
RUN tar xvfz cforth.tgz && rm cforth.tgz
WORKDIR /cforth/build/host-serial-linux64

ENTRYPOINT ["/cforth/build/host-serial-linux64/forth"]
