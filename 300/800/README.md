# 800 - Add-on Configuration

Each add-on is stored in a folder. The file structure looks like this:

```
addon_name (here: hello_world)/
  translations/
    en.yml
  apparmor.txt
  build.yml
  CHANGELOG.md
  config.yml
  DOCS.md
  Dockerfile
  icon.png
  logo.png
  README.md
  run.sh
```

**NOTE**: Translation files, ```config``` and ```build``` all support ```.json```, ```.yml``` and ```.yaml``` as the file type.

To keep it simple all examples use ```.yml```.

## 100 - Add-on script

See [README.md](./100/README.md)

## 200 - Add-on Dockerfile

See [README.md](./200/README.md)

## 300 - Add-on configuration

See [README.md](./300/README.md)

MORE ...
