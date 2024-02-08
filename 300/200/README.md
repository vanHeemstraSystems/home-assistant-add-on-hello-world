# 200 - Step 2: Installing and testing your add-on

Now comes the fun part, time to open the Home Assistant UI and install and run your add-on.

- Open the Home Assistant frontend
- Go to "**Settings**"
- Click on "**Add-ons**"
- Click "**ADD-ON STORE**" in the bottom right corner.

[
![Open your Home Assistant instance and show the Supervisor add-on store.](https://my.home-assistant.io/badges/supervisor_store.svg)](https://my.home-assistant.io/redirect/supervisor_store/)

- On the top right overflow menu (:), click the "**Check for updates**" button
- Refresh your webpage when needed
- You should now see a new section at the top of the store called "**Local add-ons**" that lists your add-on!

![Hello_World_Local_Add-on](https://github.com/vanHeemstraSystems/home-assistant-add-on-hello-world/assets/1499433/4154e1f2-6569-45ff-848b-863959bce9d2)

- Click on your add-on to go to the add-on details page.
- Install your add-on by clicking **INSTALL**.
- Start your add-on by clicking **START**.
- Click on the "**Logs**" tab, and refresh the logs of your add-on, you should now see "Hello world!" in your logs.

```
s6-rc: info: service s6rc-oneshot-runner: starting
s6-rc: info: service s6rc-oneshot-runner successfully started
s6-rc: info: service fix-attrs: starting
s6-rc: info: service fix-attrs successfully started
s6-rc: info: service legacy-cont-init: starting
s6-rc: info: service legacy-cont-init successfully started
s6-rc: info: service legacy-services: starting
s6-rc: info: service legacy-services successfully started
Hello world!
s6-rc: info: service legacy-services: stopping
s6-rc: info: service legacy-services successfully stopped
s6-rc: info: service legacy-cont-init: stopping
s6-rc: info: service legacy-cont-init successfully stopped
s6-rc: info: service fix-attrs: stopping
s6-rc: info: service fix-attrs successfully stopped
s6-rc: info: service s6rc-oneshot-runner: stopping
s6-rc: info: service s6rc-oneshot-runner successfully stopped
```

MORE ...
