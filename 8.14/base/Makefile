NAME = pblittle/docker-rsyslog
VERSION = 0.1.0

.PHONY: default
default: run

.PHONY: build
build:
	docker build --rm -t $(NAME):$(VERSION) .

.PHONY: run
run: build
	docker run -d --name rsyslog $(NAME):$(VERSION)

.PHONY: shell
shell:
	docker exec -ti rsyslog /bin/bash
