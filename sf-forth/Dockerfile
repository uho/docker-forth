FROM debian 
RUN dpkg --add-architecture i386
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
     apt-get install -qy wget sudo libc6 \
     libc6-i386 lib32stdc++6 \
  && apt-get clean \
  && rm -rf /var/lib/apt
RUN wget http://downloads.sourceforge.net/spf/spf-4.20.tar.gz \
  && tar xfz spf-4.20.tar.gz
RUN wget http://downloads.sourceforge.net/spf/spf-devel-4.20.tar.gz \
  && tar xfz spf-devel-4.20.tar.gz
WORKDIR /spf-4.20
RUN mkdir /src
VOLUME /src
#WORKDIR /src
ENTRYPOINT ["/spf-4.20/spf4orig"]
