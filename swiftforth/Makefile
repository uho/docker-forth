image:
	docker build -t swiftforth .

run:
	@# SwiftForth issues a segmentation fault when invoked w/o parameters
	@# docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src swiftforth 
	@docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src swiftforth \
          .version cr .\( Startup workaround --- Press any key to start: \) key drop

check:
	@# SwiftForth issues a segmentation fault when invoked w/o parameters
	@docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src swiftforth 

xlerb:
	echo bye | docker run --rm -i -v $(HOME)/Projects/docker-forth/src:/src  swiftforth xlerb.fs 
