UID ?= $(shell id -u)
GID ?= $(shell id -g)

.PHONY: show-config
show-config:
	@echo "UID: $(UID)"
	@echo "GID: $(GID)"

.PHONY: pre-requisites
pre-requisites:
	sudo mkdir -p /opt/clearml/data/elastic_7
	sudo mkdir -p /opt/clearml/data/mongo_4/db
	sudo mkdir -p /opt/clearml/data/mongo_4/configdb
	sudo mkdir -p /opt/clearml/data/redis
	sudo mkdir -p /opt/clearml/logs
	sudo mkdir -p /opt/clearml/config
	sudo mkdir -p /opt/clearml/data/fileserver

	sudo chown -R $(UID):$(GID) /opt/clearml
	@ls -al /opt/clearml

.PHONY: clearml-server-up
clearml-server-up: pre-requisites
	cp -rf ./config/* /opt/clearml/config/
	docker compose up -d

.PHONY: cleanup
cleanup:
	docker compose down -v
	sudo rm -rf /opt/clearml
