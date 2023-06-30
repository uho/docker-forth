FROM alpine
RUN wget https://www.complang.tuwien.ac.at/forth/gforth/Snapshots/current/gforth.tar.xz
RUN tar xvfJ gforth.tar.xz 
WORKDIR gforth-0.7.9_20230629/
RUN ./install-deps.sh 
RUN ./configure && make && make install
RUN mkdir /src
WORKDIR /src
ENTRYPOINT ["gforth"]
