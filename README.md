bogdanbrudiu/vagrant-wordpress
============================

This repository allows you to setup an Wordpress install using
vagrant for development and testing.

# Requirements

* [Virtual Box](https://www.virtualbox.org/)
* [Vagrant](http://www.vagrantup.com/)

# Installation

```bash
git clone --recursive https://github.com/bogdanbrudiu/vagrant-wordpress.git
cd vagrant-wordpress
git submodule init
git submodule update
```

For a specific Wordpress version:

```bash
cd web
git tag -l
git checkout tags/4.0
```

Start the VM:

```bash
vagrant up
```




Open your browser to 127.0.0.1:8081 and go through the Wordpress installation
wizard.

# Configuration

This setup will install mysql and create the database for you. During the
Wordpress install, it will ask for your database information. There is
no password and the username is `root`. The database name is `wordpress`

# Just a kindly reminder

If you are behind a proxy please remember to add the proxy settings to your wp-config.php file 

```
define('WP_PROXY_HOST', 'my.proxy.com');
define('WP_PROXY_PORT', '80');
```
