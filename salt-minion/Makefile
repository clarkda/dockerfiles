IMAGE_NAME=salt-minion
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
	docker run --detach=true --link salt-master:salt $(IMAGE_NAME):$(IMAGE_VERSION) -l debug

.PHONY: build clean deploy run
