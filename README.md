Dokku provisioning plugin
-------------------------

Project: https://github.com/progrium/dokku

Installation
------------
```
git clone https://github.com/Kloadut/dokku-provisioning-plugin /var/lib/dokku/plugins/provisioning
```

Usage
-----

You hust have to add a bash script named `provisioning/pre-build` at the root of your app package. It will be executed on pre-build.

```
cd /path/to/my/app
mkdir provisioning
echo "apt-get install package-name" > provisioning/pre-build
git add provisioning
git commit -m "Add provisioning script"
git push dokku master
```
