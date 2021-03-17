### Docker-Forth Mecrisp-Stellaris

Native code 32 Bit interactive Forth system by Matthis Koch

Homepage: http://mecrisp.sourceforge.net/

Version supported here: mecrisp-stellaris-2.5.6.tar.gz

#### Pull image form dockerhub

    docker pull rundockerforth/mecrisp-stellaris

#### Run from image:

    docker run -i -t --rm rundockerforth/mecrisp-stellaris

#### Build image locally

    make image

#### Run local image with repositories `src` directory mounted as `/src`

    make run

#### Run Test program `src/xlerb.fs`

    make xlerb

