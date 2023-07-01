image:
	docker build -t my4th .

run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src my4th

xlerb:
	echo include /src/xlerb.fs bye | tr \\n \\r | docker run -i --rm -v $(HOME)/Projects/docker-forth/src:/src my4th 

