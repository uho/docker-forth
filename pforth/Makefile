image:
	docker build -t pforth .

run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src pforth

xlerb:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src pforth /src/xlerb.fs 
