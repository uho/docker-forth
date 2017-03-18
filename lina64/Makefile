image:
	docker build -t lina64 .
run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src lina64

xlerb:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src lina64 -f 'S" /src/XLERB_.FS" INCLUDED BYE'
