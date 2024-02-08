# 300 - Step 3: Hosting a server

Until now we've been able to do some basic stuff, but it's not very useful yet. So let's take it one step further and host a server that we expose on a port. For this we're going to use the built-in HTTP server that comes with Python 3.

To do this, we will need to update our files as follows:

- ```Dockerfile```: Install Python 3
- ```config.yaml```: Make the port from the container available on the host
- ```run.sh```: Run the Python 3 command to start the HTTP server

Update your ```Dockerfile```:

```
ARG BUILD_FROM
FROM $BUILD_FROM

# Install requirements for add-on
RUN \
  apk add --no-cache \
    python3

# Python 3 HTTP Server serves the current working dir
# So let's set it to our add-on persistent data directory.
WORKDIR /data

# Copy data for add-on
COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
```

Dockerfile

Add "ports" to ```config.yaml```. This will make TCP on port 8000 inside the container available on the host on port 8000.

**IMPORTANT**: Notice that we update the ```version``` (was 1.0.0, now 1.1.0), to let Home Assistant know that we have made changes to this addon.

```
name: "Hello world"
description: "My first real add-on!"
version: "1.1.0"
slug: "hello_world"
init: false
arch:
  - aarch64
  - amd64
  - armhf
  - armv7
  - i386
startup: services
ports:
  8000/tcp: 8000
```

config.yaml

Update run.sh to start the Python 3 server:

```
#!/usr/bin/with-contenv bashio

echo "Hello world!"

python3 -m http.server 8000
```

run.sh

Now if using a terminal, go to the addons directory:

```
$ cd /addons
```

And pull the latest changes of this repository;

```
$ cd hello_world
$ git pull
```

Your changes should now be reflected in your Home Assistant instance.
