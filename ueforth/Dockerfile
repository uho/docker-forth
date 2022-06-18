FROM debian:bullseye-slim 
RUN mkdir /src
VOLUME /src
WORKDIR /src
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive \
  apt-get install -qy automake libtool libtool-bin g++ make wget bzip2 git nodejs python3 \
  && apt-get clean \
  && rm -rf /var/lib/apt
RUN ln -s `which python3` /usr/bin/python
WORKDIR /
RUN git clone https://github.com/flagxor/ueforth.git
WORKDIR ueforth
RUN make
WORKDIR /src
ENTRYPOINT ["/ueforth/out/posix/ueforth"]
