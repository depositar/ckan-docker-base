# Pre-configured CKAN Docker images for the depositar

This is the Git repo of the CKAN Docker images for [CKAN](https://github.com/ckan/ckan/) powering the [depositar](https://data.depositar.io/).

The images will usually be used as a Docker Compose install in conjunction with other Docker images that make up the depositar.

The depositar Docker install is located here: [depositar-docker](https://github.com/depositar/depositar-docker)

### Building and Pushing the images

    docker build -t depositar/ckan-base ckan-2.9/base
