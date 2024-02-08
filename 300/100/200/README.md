# 200 - The ```config.yaml``` file

This is your add-on configuration, which tells the Supervisor what to do and how to present your add-on.

For an overview of all valid add-on configuration options have a look [here](https://developers.home-assistant.io/docs/add-ons/configuration#add-on-configuration).

```
name: "Hello world"
description: "My first real add-on!"
version: "1.0.0"
slug: "hello_world"
init: false
arch:
  - aarch64
  - amd64
  - armhf
  - armv7
  - i386
```

hello_world/config.yaml
