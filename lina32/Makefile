image:
	docker build -t lina32 .
run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src lina32

xlerb:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src lina32 -f 'S" /src/XLERB_.FS" INCLUDED BYE'
