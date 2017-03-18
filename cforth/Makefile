image:
	docker build -t cforth .

run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src cforth

xlerb:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src cforth /src/xlerb.fs 
