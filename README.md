## images
https://hub.docker.com/u/devcm

```shell
docker build --no-cache ./ -t ${IMAGE_TAG}:latest -t ${IMAGE_TAG}:${VERSION} --build-arg VERSION="${VERSION}"
```
