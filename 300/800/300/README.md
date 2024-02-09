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

| Key | Type | Description |
| -- | -- | -- |
| ```name``` | string | The name of the add-on. |
| ```version``` | string | Version of the add-on. If you are using a docker image with the ```image``` option, this needs to match the tag of the image that will be used. |
| ```slug``` | string | Slug of the add-on. This needs to be unique in the scope of the [repository](https://developers.home-assistant.io/docs/add-ons/repository) that the add-on is published in and URI friendly. |
| ```description``` | string | Description of the add-on. |
| ```arch``` | list | A list of supported architectures: ```armhf```, ```armv7```, ```aarch64```, ```amd64```, ```i386```. |


MORE ...
