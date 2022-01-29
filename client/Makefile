build-dev:
	docker build -f Dockerfile.dev -t mean-complex-client .

export ROOT_DIR=${PWD}
run-dev:
	docker run -p 3000:3000 -v /app/node_modules -v ${ROOT_DIR}:/app mean-complex-client