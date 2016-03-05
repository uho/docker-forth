image:
	docker build -t swiftforth .
run:
	docker run --rm -i -t -v $HOME/Projects/docker-forth/src:/src swiftforth

xlerb:
	echo bye | docker run --rm -i -v $HOME/Projects/docker-forth/src:/src  swiftforth xlerb.fs 
