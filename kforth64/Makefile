image:
	docker build -t kforth .
run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src kforth 

xlerb:
	echo bye | docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src kforth xlerb.fs
