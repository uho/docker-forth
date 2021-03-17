ROOT_DIR:=$(dir $(realpath $(firstword $(MAKEFILE_LIST))))
SRC=$(ROOT_DIR)../src

show:
	echo $(ROOT_DIR)
	echo $(SRC)

image:
	docker build -t mecrisp-stellaris .
run:
	docker run --rm -i -t -v $(SRC):/src mecrisp-stellaris

xlerb:
	@echo ": .( [char] ) parse type immediate ;" `cat $(SRC)/xlerb.fs` bye  | docker run -i --rm mecrisp-stellaris qemu-arm-static mecrisp-stellaris-linux

