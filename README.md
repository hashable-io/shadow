Shadow
------------

_Shadow_ provides a a set of scripts to aid in the deployment
and maintenance of blogs deployed using Docker.

## Getting Started

First time
```
# Generate the base Dockerfiles for Running Containerized Ghost
./make_dockerfile

# Genrate the base Config files for Ghost
./make_configs

# Build & Run the Ghost Instance (Default: development)
./build_docker_image
./run_instance
# Visit: localhost:2368 (default)

# Kill Any Running Instance of Ghost
./kill_instance
```

## Building & Running Production

After editing `config.production.json` run the build and run commands and follows
```bash
//
ENV_TAG=production ./build_docker_image
# ...then push image to repository.

# ...pull image and run instance in prod:
ENV_TAG=production ./run_instance
```