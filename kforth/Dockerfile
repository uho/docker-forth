FROM debian 
RUN dpkg --add-architecture i386
RUN apt-get update -q 
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install \
   binutils:i386 gcc:i386 g++:i386 \
   make libreadline6:i386 libreadline6-dev:i386 libncurses5:i386 libncurses5-dev:i386 patchutils wget
RUN DEBIAN_FRONTEND=noninteractive && apt-get clean && rm -rf /var/lib/apt

RUN wget ftp://ccreweb.org/software/kforth/linux/kforth-x86-linux-1.5.3.tar.gz
RUN tar xfz kforth-x86-linux-1.5.3.tar.gz
WORKDIR kforth-1.5.3

RUN make && cp kforth kforth-fast /usr/bin
RUN mkdir /src
VOLUME /src
WORKDIR /src
ENTRYPOINT ["/usr/bin/kforth-fast"]

