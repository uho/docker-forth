image:
	docker build -t gforth-current .

run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src gforth-current

xlerb:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src gforth-current xlerb.fs -e bye
