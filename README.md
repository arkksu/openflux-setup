# openflux exit node

0. installed docker via
```bash
sudo curl -fsSL https://get.docker.com | sh

# additional
sudo usermod -aG docker $USER
newgrp docker
```

1. generate encryption secret
```bash
openssl rand -hex 32 > .secret.key
chmod 600 .secret.key
```

2. edit `compose.yaml` to set `--url` or `--transport`
```bash
nano compose.yaml
```

3. useful universal command
```bash
docker compose down && docker compose up -d && docker compose logs -ft
```

you'll see openflux:// link and QR there, just CTRL+C to exit logs