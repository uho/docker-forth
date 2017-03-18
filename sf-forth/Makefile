image:
	docker build -t sf-forth .
run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src sf-forth

xlerb:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src  sf-forth 'S" /src/XLERB_.FS" INCLUDED BYE'
