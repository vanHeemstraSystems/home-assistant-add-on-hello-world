# 100 - The ```Dockerfile``` file

This is the image that will be used to build your add-on.

```
ARG BUILD_FROM
FROM $BUILD_FROM

# Copy data for add-on
COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
```

Dockerfile
