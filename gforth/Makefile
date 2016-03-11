image:
	docker build -t gforth .
run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src gforth 

xlerb:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src gforth xlerb.fs -e bye
