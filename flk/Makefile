image:
	docker build -t flk .
run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src flk

xlerb:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src flk xlerb.fs -e bye
