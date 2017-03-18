FROM debian 
RUN dpkg --add-architecture i386

RUN apt-get update && apt-get -y upgrade
RUN apt-get -y install gcc:i386 libc6-dev:i386 \
   make wget vim libncurses5-dev:i386 git

# Install 32 bit gforth (working around missing dependency emacsen-commen:i386)
RUN apt-get -y install libffcall1:i386 libltdl7:i386 gforth-common:i386 gforth-lib:i386
RUN wget http://ftp.de.debian.org/debian/pool/main/g/gforth/gforth_0.7.2+dfsg1-1.1_i386.deb
RUN dpkg --force-all -i gforth_0.7.2+dfsg1-1.1_i386.deb

RUN apt-get clean  && rm -rf /var/lib/apt

WORKDIR /
RUN git clone https://github.com/uho/flk.git
WORKDIR /flk

RUN make depend
RUN make clean

ENV TERM=vt100
RUN make FORTH32="gforth -e"
RUN make FORTH32="gforth -e" install

RUN mkdir /src
VOLUME /src
WORKDIR /src
ENTRYPOINT ["/usr/local/bin/flk"]
