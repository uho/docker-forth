FROM debian 
RUN dpkg --add-architecture i386
RUN apt-get update -q 
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install \
   binutils:i386 gcc:i386 g++:i386 \
   make libreadline7:i386 libreadline-dev:i386 libncurses5:i386 libncurses5-dev:i386 patchutils wget git
RUN DEBIAN_FRONTEND=noninteractive && apt-get clean && rm -rf /var/lib/apt

RUN git clone https://github.com/mynenik/kForth-32.git
WORKDIR kForth-32/src

RUN make && cp kforth32 kforth32-fast /usr/bin
RUN mkdir /src
VOLUME /src
WORKDIR /src
ENTRYPOINT ["/usr/bin/kforth32-fast"]

