image:
	docker build -t ueforth .
run:
	docker run --rm -i -t -v $(HOME)/Projects/docker-forth/src:/src ueforth

xlerb:
	echo ': .( [char] ) parse type ; immediate include xlerb.fs bye' | \
	    docker run --rm -i -v $(HOME)/Projects/docker-forth/src:/src ueforth
