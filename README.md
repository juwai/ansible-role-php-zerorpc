Ansible Role: php-zerorpc
=========

Install PHP extensions required by php-zerorpc on CentOS servers:

+ msgpack
+ zmq

Requirements
------------

Written in Ansible 2.3.*

Please make sure PHP pecl command installed.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

### msgpack_source_version

Commit, tag, or branch of msgpack PHP extension to use when installing from source.

Default is `msgpack-2.0.2`.

### pecl_msgpack_version

MessagePack PHP extension version.

Default is `0.5.7`.

### pecl_zmq_version

ZeroMQ PHP extension version.

Default is `1.1.2`.

### php_extensions_config_path

Path of folder containing PHP extension config files.

Default is `/etc/php.d`.

### php_fpm_daemon

php_fpm daemon's name.

Default is `php-fpm`.

### php_opcache_config_filename

PHP opcache extension config filename.

Default is `10-opcache.ini`.

### php_zerorpc_segfault_fix

Enable to avoid segfault in PHP7 with opcache.

Default is `false`.

### zmq_source_version

Commit, tag, or branch of zmq PHP extension to use when installing from source.

Default is `f2617063a4c007ca6073c0d09e9f36fd9b87ddaf`.

Dependencies
------------

juwai.libzmq

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: juwai.php-zerorpc

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2016 by [Juwai Limited](http://www.juwai.com).
