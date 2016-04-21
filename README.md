# ansible-postgis3d [![Build Status](https://travis-ci.org/Oslandia/ansible-postgis3d.svg?branch=master)](https://travis-ci.org/Oslandia/ansible-postgis3d)

Tested on debian (jessie, sid) and ubuntu trusty 1404

What will be installed:

- postgresql **9.5** from the official postgresql repository
- sfcgal **1.3.0** release pulled from github
- pointcloud **master** branch pulled from github
- pdal **1.1.0** release pulled from github
- postgis **2.2.1** release pulled from osgeo repository


## Role Variables

    * build_directory: location to where the sources will be downloaded and compiled
      (should be a non superuser directory)

The next variables could be overrided if you need some specific versions:

    * postgis_version
    * sfcgal_version
    * pointcloud_version
    * pdal_version


## How to use it

* Provision your local machine:

```bash
ansible-playbook -i 'localhost,' -e "build_directory=/home/me/apps/postgis3d" --ask-become -c local test.yml
```

* Pull this role from the ansible galaxy:

```bash
ansible-galaxy install Oslandia.postgis3d
```

* Test it with vagrant:

```bash
vagrant up jessie
# That's all folks ! you will have a debian jessie with postgis ready for 3D and pointcloud support.

```
Now, don't forget to configure postgresql, pg_hba.conf etc...

License
-------

GPLv3

Author Information
------------------

www.oslandia.com
