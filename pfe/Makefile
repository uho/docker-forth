image:
	docker build -t pfe .
run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src pfe

xlerb:
	echo bye | docker run --rm -i -v $(HOME)/Projects/docker-forth/src:/src pfe xlerb.fs 
