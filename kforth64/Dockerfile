FROM debian:buster 
RUN apt-get update -q 
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install \
   binutils gcc: g++ \
   make libreadline7 libreadline-dev libncurses5 libncurses5-dev patchutils wget git
RUN DEBIAN_FRONTEND=noninteractive && apt-get clean && rm -rf /var/lib/apt

RUN git clone https://github.com/mynenik/kForth-64.git
WORKDIR kForth-64/src

RUN make && cp kforth64 /usr/bin
RUN mkdir /src
VOLUME /src
WORKDIR /src
ENTRYPOINT ["/usr/bin/kforth64"]

