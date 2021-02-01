image:
	docker build -t muforth .

shell:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src muforth 

run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src muforth /muforth/mu/muforth

xlerb:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src muforth /muforth/mu/muforth ': .( char ) parse type ; z" /src/xlerb.fs" load-file'
