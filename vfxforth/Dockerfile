FROM debian:buster 
RUN dpkg --add-architecture i386
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
     apt-get install -qy wget sudo libc6-i386 lib32stdc++6 \
  && apt-get clean \
  && rm -rf /var/lib/apt
RUN wget https://vfxforth.com/downloads/VfxCommunity/VfxForth_x86_lin.tar.gz \
  && tar xfz VfxForth_x86_lin.tar.gz
WORKDIR /VfxForthLin
RUN echo bye | ./InstallMe.Lin32.sh
RUN mkdir /src
VOLUME /src
WORKDIR /src
ENTRYPOINT ["/VfxForthLin/Bin/x386Lin"]
