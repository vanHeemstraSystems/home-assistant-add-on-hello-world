# 100 - Introduction

So you've got Home Assistant going and you've been enjoying the built-in add-ons but you're missing this one application. Time to make your own add-on!

To get started with developing add-ons, we first need access to where Home Assistant looks for local add-ons. For this you can use the [Samba](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_samba) or the [SSH](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_ssh) add-ons.

For Samba, once you have enabled and started it, your Home Assistant instance will show up in your local network tab and share a folder called "addons". This is the folder to store your custom add-ons.

**TIP**: If you are on macOS and the folder is not showing up automatically, go to Finder and press CMD+K then enter ```smb://homeassistant.local```

For SSH, you will have to install it. Before you can start it, you will have to have a private/public key pair and store your public key in the add-on config ([see docs for more info](https://github.com/home-assistant/addons/blob/master/ssh/DOCS.md#configuration)). Once started, you can SSH to Home Assistant and store your custom add-ons in the ```/addons``` directory.

Once you have located your add-on directory, it's time to get started!
