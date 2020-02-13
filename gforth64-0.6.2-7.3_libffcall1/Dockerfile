# Rebuild Gforth 0.6.2 with libffcall support  uh 2020-02-13

# ------------------------------------
FROM lpenz/debian-lenny-amd64-minbase as builder

RUN echo deb-src http://archive.debian.org/debian lenny main >>/etc/apt/sources.list
RUN apt-get update -q 

# Install missing ffcall dependency
RUN apt-get -y --force-yes install libffcall1 libffcall1-dev

# Install tools required for gforth
RUN apt-get -y --force-yes install gforth
RUN apt-get -y --force-yes install dpkg-dev
RUN apt-get -y --force-yes source gforth
RUN apt-get -y --force-yes build-dep gforth

# switch to source dir
WORKDIR /gforth-0.6.2

# Apply patch from Gforth home page
COPY comp-i.patch .
RUN patch <comp-i.patch
COPY 0.6.2-ffcall-64bit.diff .
RUN patch -p0 <0.6.2-ffcall-64bit.diff
RUN touch engine/*.i kernel/aliases.fs kernel/prim.fs

# Build Debian Package
RUN dpkg-buildpackage -uc -b

# Provide correct package name
RUN mv /gforth_0.6.2-7.3_amd64.deb /gforth_0.6.2-7.3_libffcall1_amd64.deb

# ------------------------------------
FROM lpenz/debian-lenny-amd64-minbase 
RUN apt-get update -q 

# Now use the new package
RUN apt-get -y --force-yes install libffcall1
COPY --from=builder /gforth_0.6.2-7.3_libffcall1_amd64.deb \
                    /gforth_0.6.2-7.3_libffcall1_amd64.deb
RUN dpkg -i /gforth_0.6.2-7.3_libffcall1_amd64.deb
RUN rm /gforth_0.6.2-7.3_libffcall1_amd64.deb

# Shared directory with guest
RUN mkdir /src
VOLUME /src
WORKDIR /src

# CMD "/usr/bin/gforth"
ENTRYPOINT ["/usr/bin/gforth"]

