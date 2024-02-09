# 100 - Required configuration options

| Key | Type | Description |
| -- | -- | -- |
| ```name``` | string | The name of the add-on. |
| ```version``` | string | Version of the add-on. If you are using a docker image with the ```image``` option, this needs to match the tag of the image that will be used. |
| ```slug``` | string | Slug of the add-on. This needs to be unique in the scope of the [repository](https://developers.home-assistant.io/docs/add-ons/repository) that the add-on is published in and URI friendly. |
| ```description``` | string | Description of the add-on. |
| ```arch``` | list | A list of supported architectures: ```armhf```, ```armv7```, ```aarch64```, ```amd64```, ```i386```. |
