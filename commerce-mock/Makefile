RELEASE=0.0.1
APP=commerce-mock
DOCKER_ACCOUNT=<YOUR DOCKER ID>
CONTAINER_IMAGE=${DOCKER_ACCOUNT}/${APP}:${RELEASE}

.PHONY: build-image push-image

build-image:
	docker build -t $(CONTAINER_IMAGE) --no-cache --rm .

push-image: build-image
	docker push $(CONTAINER_IMAGE)

docker-run:
	docker run -it --rm -p 10000:10000 $(CONTAINER_IMAGE)