FROM debian:bullseye-slim 
RUN mkdir /src
VOLUME /src
WORKDIR /src
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
  apt-get install -qy build-essential wget unzip \
  && apt-get clean \
  && rm -rf /var/lib/apt
WORKDIR /

RUN wget http://mynor.org/downloads/my4th-tool-v1.1.zip
RUN unzip my4th-tool-v1.1.zip
WORKDIR /my4th-tool-v1.1
RUN tar xvfz sources.tgz
WORKDIR /my4th-tool-v1.1/source
RUN make 
RUN cp my4th /

WORKDIR /
RUN wget http://mynor.org/downloads/my4th-rom-v1.2.zip
RUN unzip my4th-rom-v1.2.zip
RUN cp /my4th-rom-v1.2/my4th-rom_8MHz_v1.2.bin /my4th-rom.bin

WORKDIR /
ENTRYPOINT [ "/my4th", "-t" ]
