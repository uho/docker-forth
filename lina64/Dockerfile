FROM debian 
RUN dpkg --add-architecture i386
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
     apt-get install -qy wget sudo libc6-i386 lib64stdc++6 \
  && apt-get clean \
  && rm -rf /var/lib/apt
RUN wget http://home.hccnet.nl/a.w.m.van.der.horst/lina64-5.3.0.tar.gz \
  && tar xfz lina64-5.3.0.tar.gz
WORKDIR /lina64-5.3.0
RUN mkdir /src
VOLUME /src
# WORKDIR /src
ENTRYPOINT ["/lina64-5.3.0/lina64"]
