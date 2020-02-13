image:
	docker build -t gforth64-0.6.2-7.3 .

deb:
	docker build --target builder -t gforth64-0.6.2-7.3-deb .
	docker run --rm gforth64-0.6.2-7.3-deb cat /gforth_0.6.2-7.3_libffcall1_amd64.deb >gforth_0.6.2-7.3_libffcall1_amd64.deb

run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src gforth64-0.6.2-7.3 

xlerb:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src gforth64-0.6.2-7.3 xlerb.fs -e bye
