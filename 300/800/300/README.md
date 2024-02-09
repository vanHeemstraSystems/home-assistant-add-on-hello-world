# 300 - Add-on configuration

The configuration for an add-on is stored in ```config.yml```.

```
name: "Hello world"
version: "1.1.0"
slug: folder
description: >-
  "Long description"
arch:
  - amd64
url: "website with more information about the add-on (e.g., a forum thread for support)"
ports:
  123/tcp: 123
map:
  - config:rw
  - ssl
image: repo/{arch}-my-custom-addon
```

config.yml

**NOTE**: Avoid using ```config.yml``` as filename in your add-on for anything other than the add-on configuration. The Supervisor does a recursively search for ```config.yml``` in the add-on repository.

## 100 - Required configuration options

See [README.md](./100/README.md)

## 200 - Optional configuration options

See [README.md](./300/README.md)

MORE ...
