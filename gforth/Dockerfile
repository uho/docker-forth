FROM debian 
RUN mkdir /src
VOLUME /src
WORKDIR /src
RUN apt-get update -q \
  && DEBIAN_FRONTEND=noninteractive apt-get install -qy gforth \
  && apt-get clean \
  && rm -rf /var/lib/apt
ENTRYPOINT ["gforth"]
