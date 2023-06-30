image:
	docker build -t gforth-alpine .
run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src gforth-alpine

xlerb:
	echo bye | docker run --rm -i -v $(HOME)/Projects/docker-forth/src:/src gforth-alpine xlerb.fs 
