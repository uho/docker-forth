FROM debian 
RUN dpkg --add-architecture i386

RUN apt-get update && apt-get -y upgrade
RUN apt-get -y install gcc:i386 libc6-dev:i386 \
   make wget vim libncurses5-dev:i386 git

RUN apt-get clean  && rm -rf /var/lib/apt

WORKDIR /
RUN git clone https://github.com/uho/minforth.git
WORKDIR /minforth

RUN yes | make

ENV TERM=vt100

RUN mkdir /src
VOLUME /src
WORKDIR /src
ENTRYPOINT ["/minforth/miniforth", "-i", "/minforth/miniforth.i"]
