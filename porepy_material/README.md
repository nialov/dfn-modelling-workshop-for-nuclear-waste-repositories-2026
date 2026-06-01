# PorePy workshop container

## Build

```bash
docker build -t ghcr.io/nialov/porepy-notebook .
```

## Push to GHCR

Use a **GitHub personal access token (classic)**.

Required scope for push:
- `write:packages`

Recommended minimal set:
- `write:packages`
- `read:packages`

Optional, only if you also want to delete package versions later:
- `delete:packages`

Your GitHub user must also have permission to publish the package under the target owner/namespace.

```bash
echo '<GH_TOKEN>' | docker login ghcr.io -u <github-user> --password-stdin
docker push ghcr.io/nialov/porepy-notebook
```

## Run with Docker Compose

```bash
docker compose up --build
```
