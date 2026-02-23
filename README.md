# ClearML PoC

This repository is a PoC for ClearML, an open-source MLOps platform.
Currently just following official docs is quite difficult to understand overall ML workflow for user who just want to quickly try out ClearML as client.  
You can simply reproduce the whole ClearML platform and workload in this single repository.

This repository is divided into three main components by following exactly as maintainers intended.

![clearml-overview](https://raw.githubusercontent.com/clearml/clearml-docs/main/docs/img/clearml_architecture.png)

- [x] [./clearml-client](./clearml-client/README.md): Examples of using ClearML SDK as client, and how it interacts with ClearML Server and external storage for artifact management.
- [x] [./clearml-server](./clearml-server/README.md): A compose.yaml to setup ClearML Server OSS with docker compose.
- [ ] ./clearml-agent: Examples of using ClearML Agent for handling multiple tasks as queue and executing them in multiple machines.

## Why ClearML?

Most of the MLOps platforms have below constraints.

- Too over-engineered when considering objective (ML workflow) (***e.g.*** limited deployment options, complex infra like k8s)
- Too computer-science/software-product-lifecycle oriented Ops, which is not friendly for data scientists and ML engineers.
  - Git based version control for code and data, which is not intuitive for target-users and hard to manage experiments when combinatorial explosion happens.
- Vendor lock-in for users who want to use the platform as a service,
- Quite expensive subscription fee for small teams.

## References

- clearml-sdk(client): https://github.com/clearml/clearml
- clearml-server: https://github.com/clearml/clearml-server
- clearml-agent: https://github.com/clearml/clearml-agent
- clearml-docs: https://clear.ml/docs/latest/docs/
