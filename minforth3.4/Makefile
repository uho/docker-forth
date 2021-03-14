image:
	docker build -t minforth34 .

run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src minforth34

xlerb:
	echo include /src/xlerb.fs bye | tr \\n \\r | docker run -i --rm -v $(HOME)/Projects/docker-forth/src:/src minforth34 

