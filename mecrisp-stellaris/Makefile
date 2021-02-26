image:
	docker build -t mecrisp-stellaris .
run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src mecrisp-stellaris

xlerb:
	@echo ": .( [char] ) parse type immediate ;" `cat $(HOME)/Projects/docker-forth/src/xlerb.fs` bye  | docker run -i --rm mecrisp-stellaris qemu-arm-static mecrisp-stellaris-linux

