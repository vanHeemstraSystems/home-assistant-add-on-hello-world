# 200 - Add-on Dockerfile

All add-ons are based on the latest Alpine Linux image. Home Assistant will automatically substitute the right base image based on the machine architecture. Add ```tzdata``` if you need to run in a different timezone. ```tzdata``` Is is already added to our base images.

```
ARG BUILD_FROM
FROM $BUILD_FROM

# Install requirements for add-on
RUN \
  apk add --no-cache \
    example_alpine_package

# Copy data for add-on
COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
```

If you don't use local build on the device or our build script, make sure that the Dockerfile also has a set of labels that include:

```
LABEL \
  io.hass.version="VERSION" \
  io.hass.type="addon" \
  io.hass.arch="armhf|aarch64|i386|amd64"
```

It is possible to use your own base image with ```build.yml``` or if you do not need support for automatic multi-arch building you can also use a simple docker ```FROM```. You can also suffix the Dockerfile with the specific architecture to use a specific Dockerfile for a particular architecture, i.e. ```Dockerfile.amd64```.

## 100 - Build Args

See [README.md](./100/README.md)
