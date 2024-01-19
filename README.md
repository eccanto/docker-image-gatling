# Gatling Docker Images

This repository provides Dockerfiles for building Gatling load testing tools within Docker containers.

## Available Images

The following Gatling versions are currently available:

* [3.8.4-alpine](./3.8.4-alpine/Dockerfile)
* [3.9.5-alpine](./3.9.5-alpine/Dockerfile)
* [3.10.3-alpine](./3.10.3-alpine/Dockerfile)

## Usage

## Building Images:

Run the following command to build an image (e.g., `cd 3.10.3-alpine`):

```bash
docker build -t eccanto/gatling:3.10.3-alpine 3.10.3-alpine
```

To publish the image:

```bash
docker push eccanto/gatling:3.10.3-alpine
```

## Running Gatling:

Example using Docker compose: [Performance testing using Gatling (Java and Scala)](https://github.com/eccanto/base-performance-testing-gatling)

## Customization

Modify the Dockerfiles to adjust base images, software installations, or configurations as needed.

## Additional Information

Docker Hub: Images are published on Docker Hub as [eccanto/gatling:VERSION](https://hub.docker.com/repository/docker/eccanto/gatling/tags).

Gatling Documentation: Refer to Gatling's official documentation for comprehensive usage and configuration details:
https://gatling.io/docs/

## Contributing

Pull requests are welcome for adding new Gatling versions or enhancements.

## License

[MIT](./LICENSE)
