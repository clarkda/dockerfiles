IMAGE_NAME=salt-master
IMAGE_VERSION=latest

build:
	docker build -t $(IMAGE_NAME):$(IMAGE_VERSION) .
	# docker build -t $(IMAGE_NAME):latest .

clean:
	docker rmi -f `docker images -f "dangling=true" -q`

deploy:
	docker push $(IMAGE_NAME):$(IMAGE_VERSION)
	# docker push $(IMAGE_NAME):latest

run:
	docker run --detach=true --name=salt-master $(IMAGE_NAME):$(IMAGE_VERSION) -l debug

.PHONY: build clean deploy run
