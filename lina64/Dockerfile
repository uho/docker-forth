FROM debian:bullseye-slim 
RUN dpkg --add-architecture i386
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
     apt-get install -qy wget sudo lib64stdc++6 \
  && apt-get clean \
  && rm -rf /var/lib/apt
RUN wget https://home.hccnet.nl/a.w.m.van.der.horst/ci86.lina64-5.4.1.tar.gz \
  && tar xfz ci86.lina64-5.4.1.tar.gz
WORKDIR /ci86.lina64-5.4.1
RUN mkdir /src
VOLUME /src
# WORKDIR /src
ENTRYPOINT ["/ci86.lina64-5.4.1/lina64"]
