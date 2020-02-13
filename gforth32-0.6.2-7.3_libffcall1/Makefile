image:
	docker build -t gforth32-0.6.2-7.3 .

deb:
	docker build --target builder -t gforth32-0.6.2-7.3-deb .
	docker run --rm gforth32-0.6.2-7.3-deb cat /gforth_0.6.2-7.3_libffcall1_i386.deb >gforth_0.6.2-7.3_libffcall1_i386.deb

run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src gforth32-0.6.2-7.3 

xlerb:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src gforth32-0.6.2-7.3 xlerb.fs -e bye
