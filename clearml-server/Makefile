UID ?= $(shell id -u)
GID ?= $(shell id -g)

.PHONY: show-config
show-config:
	@echo "UID: $(UID)"
	@echo "GID: $(GID)"

.PHONY: pre-requisites
pre-requisites:
	sudo mkdir -p /opt/clearml
	sudo cp -rf ./config /opt/clearml
	sudo cp -rf ./data /opt/clearml
	sudo cp -rf ./logs /opt/clearml

	sudo chown -R $(UID):$(GID) /opt/clearml
	ls -al /opt/clearml

.PHONY: clearml-server-up
clearml-server-up: pre-requisites
	docker compose up -d

.PHONY: cleanup
cleanup:
	docker compose down -v
	sudo rm -rf /opt/clearml
