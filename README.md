# Pre-configured CKAN Docker images for the depositar

This is the repository of the official [Docker images](https://hub.docker.com/r/ckan/ckan-base/) for [CKAN](https://github.com/ckan/ckan/) powering the [depositar](https://data.depositar.io/).

The images will usually be used as a Docker Compose install in conjunction with other Docker images that make up the CKAN platform. The depositar Docker install is located here: [depositar-docker](https://github.com/depositar/depositar-docker)

### Release

Images are built and pushed to the Docker Hub after a new [release](https://github.com/depositar/ckan-docker-base/releases)
is published.

### Building the images locally

The images can be built locally for development and debugging purposes

> [!WARNING]
> Do not push images directly to the Docker Hub locally. Use the proper release process described
> above.

All operations are done using the `build.sh` script located at the root of the repository.

```
Usage: ./build.sh <action> [<params>]
Available actions:
  versions                   - Shows the current CKAN versions used
  build <version> [base|dev] - Builds images for a CKAN version
                               Pass 'base' or 'dev' to just build these.
  push  <version>            - Pushes images to the Docker Hub

```

For instance:

```
./build.sh build 2.11

./build.sh build depositar base
./build.sh build master
./build.sh build 2.10 base
./build.sh build 2.9 dev
```


