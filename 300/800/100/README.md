# 100 - Add-on script

As with every Docker container, you will need a script to run when the container is started. A user might run many add-ons, so it is encouraged to try to stick to Bash scripts if you're doing simple things.

All our images also have [bashio](https://github.com/hassio-addons/bashio) installed. It contains a set of commonly used operations and can be used to be included in add-ons to reduce code duplication across add-ons, therefore making it easier to develop and maintain add-ons.

When developing your script:

- ```/data``` is a volume for persistent storage.
- ```/data/options.json``` contains the user configuration. You can use Bashio to parse this data.

```
CONFIG_PATH=/data/options.json

TARGET="$(bashio::config 'target')"
```

So if your ```options``` contain

```
{ "target": "beer" }
```

then there will be a variable ```TARGET``` containing ```beer``` in the environment of your bash file afterwards.
