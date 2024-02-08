# 500 - Bonus: Working with add-on options

In the screenshot you've probably seen that our server only served up 1 file: ```options.json```. This file contains the user configuration for this add-on. Because we specified two empty objects for the keys "```options```" and "```schema```" in our ```config.yaml```, the resulting file is currently empty.

Let's see if we can get some data into that file!

To do this, we need to specify the default options and a schema for the user to change the options. Change the ```options``` and ```schema``` entries in your ```config.yaml``` with the following:

```
...
options:
  beer: true
  wine: true
  liquor: false
  name: "world"
  year: 2017
schema:
  beer: bool
  wine: bool
  liquor: bool
  name: str
  year: int
...
```

config.yaml

Reload the add-on store and re-install your add-on. You will now see the options available in the add-on config screen. When you now go back to our Python 3 server and download ```options.json```, you'll see the options you set. [Example of how options.json can be used inside ```run.sh```](https://github.com/home-assistant/addons/blob/master/dhcp_server/data/run.sh#L10-L13)
