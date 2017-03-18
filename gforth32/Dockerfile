FROM debian 
RUN dpkg --add-architecture i386
RUN apt-get update -q 
# Install 32 bit gforth (working around missing dependency emacsen-commen:i386)
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install \
  libffcall1:i386 libltdl7:i386 gforth-common:i386 gforth-lib:i386 wget
RUN wget http://ftp.de.debian.org/debian/pool/main/g/gforth/gforth_0.7.2+dfsg1-1.1_i386.deb
RUN dpkg --force-all -i gforth_0.7.2+dfsg1-1.1_i386.deb
RUN DEBIAN_FRONTEND=noninteractive && apt-get clean \
  && rm -rf /var/lib/apt
RUN mkdir /src
VOLUME /src
WORKDIR /src
ENTRYPOINT ["/usr/bin/gforth"]

