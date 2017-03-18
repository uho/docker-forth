image:
	docker build -t gforth32 .
run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src gforth32 

xlerb:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src gforth32 xlerb.fs -e bye
