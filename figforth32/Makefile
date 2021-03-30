ROOT_DIR:=$(dir $(realpath $(firstword $(MAKEFILE_LIST))))
SRC=$(ROOT_DIR)../src

image:
	docker build -t figforth32 .
run:
	docker run --rm -i -t -v $(SRC):/src figforth32 

xlerb:
	@echo ": .( 41 WORD HERE COUNT TYPE ; IMMEDIATE " `cat $(SRC)/XLERB_.FS` BYE | docker run --rm -i -v $(SRC):/src figforth32 
