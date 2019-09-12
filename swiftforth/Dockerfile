FROM debian 
RUN dpkg --add-architecture i386
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
     apt-get install -qy wget libc6-i386 lib32stdc++6 \
  && apt-get clean \
  && rm -rf /var/lib/apt
RUN wget http://dl.forth.com/downloads/SwiftForth-linux-macos-eval.tgz \
  && tar xfz SwiftForth-linux-macos-eval.tgz
RUN mkdir /src
VOLUME /src
WORKDIR /src
ENTRYPOINT ["/SwiftForth/bin/linux/sf"]
