FROM debian:buster-slim
RUN mkdir /src
VOLUME /src

RUN apt update -q && \
    apt upgrade -qy && \
    apt install -qy wget zip && \
    apt clean && \
    rm -rf /var/lib/apt

RUN mkdir figforth
WORKDIR figforth
RUN wget http://forth-ig.nl/downloads/files/lina2d148.zip 
RUN unzip lina2d148.zip 
RUN rm lina2d148.zip

ENTRYPOINT ["/figforth/lina"]
