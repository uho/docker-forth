FROM debian 
RUN dpkg --add-architecture i386
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
     apt-get install -qy wget sudo libc6-i386 lib32stdc++6 \
  && apt-get clean \
  && rm -rf /var/lib/apt
RUN wget ftp://public@soton.mpeforth.com/VfxLinEval/vfxforth-eval-4.72-0555.i386.tar.gz \
  && tar xfz vfxforth-eval-4.72-0555.i386.tar.gz
WORKDIR /VfxLinEval
RUN echo bye | ./InstallMe.Lin32.sh
RUN mkdir /src
VOLUME /src
WORKDIR /src
ENTRYPOINT ["/VfxLinEval/Bin/vfxlin"]
