# Solana Dev Environment Docker Image
A prebuilt Solana development environment designed for quick setup and fast iteration.

## Features
- Rust toolchain (cargo) included  
- Solana CLI installed  
- Minimal, ready-to-use image for local Solana development

## Usage

### Pull the image
Using Docker:
```bash
docker pull ghcr.io/thal-sh/solana-dev-env:latest
```
Using Podman:
```bash
podman pull ghcr.io/thal-sh/solana-dev-env:latest
```

### Run the container
To start a container with an interactive shell:
```bash
docker run --rm -it ghcr.io/thal-sh/solana-dev-env:latest bash
```
Or with Podman:
```bash
podman run --rm -it ghcr.io/thal-sh/solana-dev-env:latest bash
```

### Mount your local project directory
To work on your local Solana project inside the container, mount your project directory:
```bash
docker run --rm -it -v /path/to/your/project:/project ghcr.io/thal-sh/solana-dev-env:latest bash
```
Replace `/path/to/your/project` with your actual local path.

Inside the container, your project will be accessible at `/project`.

### Verify installation
Inside the container, check versions:
```bash
solana --version
cargo --version
```

## Notes
- The image is designed for quick setup and development speed.
- Includes all necessary tools to start building Solana apps locally.

Feel free to open issues or request features!
