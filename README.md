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
xdebug_version: 7.1      # The version of PHP that's running
xdebug_enable_mod: false # Whether to run phpenmod to enable the xdebug model
```

Settings for the `xdebug.ini` file, see [xdebug docs](https://xdebug.org/docs/all_settings):

```yaml
xdebug_conf_max_nesting_level: 256
xdebug_conf_remote_port: 9000
xdebug_conf_idekey: PHPSTORM
xdebug_conf_remote_connect_back: 0
```

Dependencies
------------

* PHP (check out [geerlingguy.php](https://github.com/geerlingguy/ansible-role-php))

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
