# ClearML Server

![clearml-server-architecture](https://clear.ml/docs/latest/assets/images/ClearML_Server_Diagram-7ea19db8e22a7737f062cce207befe38.png)

## How-to-deploy

> [!NOTE]
> Refer to https://clear.ml/docs/latest/docs/deploying_clearml/clearml_server_linux_mac
> This clearml-server is based on v2.3.0

### Pre-requisites

- Oauth2 Proxy setup (provider: GitHub)
  - Go https://github.com/settings/developers and create a new OAuth App
  - Set Homepage URL to `http://<OAUTH2_DOMAIN_NAME>/`
  - Set `Authorization callback URL` to `http://<OAUTH2_DOMAIN_NAME>/oauth2/callback`
  - Get `Client ID` and `Client Secrets`

- Copy `.env.default` to `.env` and update variables
