# QR Code Generator (Dockerized)

A Python app that generates a QR code from a URL, packaged as a Docker image.

## Run with Docker

```bash
docker pull mab263/qr-code-generator-app
docker run --rm \
  -v "$(pwd)/qr_codes:/app/qr_codes" \
  mab263/qr-code-generator-app --url http://www.njit.edu
```

## Configuration

Set these environment variables with `-e`:

- `QR_CODE_DIR`: output folder (default `qr_codes`)
- `FILL_COLOR`: QR color (default `red`)
- `BACK_COLOR`: background color (default `white`)

Example: `docker run --rm -e FILL_COLOR=blue -e BACK_COLOR=yellow mab263/qr-code-generator-app --url http://www.njit.edu`

## Build locally

```bash
docker build -t qr-code-generator-app .
```

## Links

- DockerHub: https://hub.docker.com/r/mab263/qr-code-generator-app
- CI: GitHub Actions builds and pushes the image on every push to `main`.

