# ClearML Server

![clearml-server-architecture](https://clear.ml/docs/latest/assets/images/ClearML_Server_Diagram-7ea19db8e22a7737f062cce207befe38.png)

## How-to-deploy

> [!NOTE]
> Refer to https://clear.ml/docs/latest/docs/deploying_clearml/clearml_server_linux_mac
> This clearml-server is based on v2.3.0

`docker compose up -d`
- if oauth2proxy is needed, `docker compose up -f compose.yaml -f compose.oauth2proxy.yaml -d`

### Pre-requisites
