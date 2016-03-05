image:
	docker build -t vfxforth .
run:
	docker run --rm -i -t -v $HOME/Projects/docker-forth/src:/src -t vfxforth

xlerb:
	docker run --rm -i -t -v $HOME/Projects/docker-forth/src:/src  vfxforth include xlerb.fs bye
