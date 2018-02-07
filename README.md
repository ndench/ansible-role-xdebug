Xdebug
======

[![Build Status](https://travis-ci.org/ndench/ansible-role-xdebug.svg?branch=master)](https://travis-ci.org/ndench/ansible-role-xdebug)

Ansible role to install and configure [Xdebug](https://xdebug.org) on Ubuntu.

Requirements
------------

* PHP

Role Variables
--------------

All variables are listed below, along with their default values in [defaults/main.yml](defaults/main.yml):

Variables for installing xdebug:

```yaml
# The version of the xdebug package to install (ie. php7.2-xdebug)
xdebug_php_version: 7.2

# xdbebug.ini settings
# see: https://xdebug.org/docs/all_settings

xdebug_conf_max_nesting_level: 256
xdebug_conf_idekey: PHPSTORM

# Start xdebug on every requset, regardless of the GET/POST variable
xdebug_remote_autostart: 0

# Connect to the client that sent the request
xdebug_conf_remote_connect_back: 0

# Connect to the specified host (overidden by remote_connect_back)
# 10.0.2.2 is the default IP address virtualbox assigns to the host
xdebug_remote_enable: 0
xdebug_remote_host: 10.0.2.2
xdebug_conf_remote_port: 9000
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: dev
      roles:
         - { role: ndench.xdebug }

License
-------

MIT

Author Information
------------------

This role was created in 2017 by [Nathan Dench](https://www.linkedin.com/in/nathandench/).
