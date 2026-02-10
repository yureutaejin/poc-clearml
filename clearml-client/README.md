# ClearML Client

## Getting Started

1. In root directory, run:

```bash
uv sync --group client
```

2. Run the ClearML setup script

```bash
clearml-init
```

3. Go to `{YOUR_CLEARML_SERVER_DOMAIN}/login` and sign in/up
  - ClearML Server OSS might need pre-created users by admin (Refer to [../clearml-server/config/apiserver.conf.default](../clearml-server/config/apiserver.conf.default))

4. Go to `Settings` -> `Workspace` and create new API credentials
