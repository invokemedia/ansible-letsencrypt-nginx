Ansible Letsencrypt Nginx
=========================

> Ansible script that installs letsencrypt and adds a domain

Requirements
------------

This role assumes you already have nginx installed and you are not going to be setting up more than 1 domain on the server.

Installation
------------

`git clone https://github.com/invokemedia/ansible-letsencrypt-nginx roles/invokemedia.letsencrypt-nginx`

Role Variables
--------------

```
# the root of the public site
letsencrypt_root: /var/www/html/public
# the domain we are adding
letsencrypt_domain: example.com
# the email to use for letsencrypt
letsencrypt_email: email@example.com
```

Dependencies
------------

None.

Example Playbook
-------------------------

Here is how you would use the default setup setup.

```
- hosts: web
  sudo: yes
  vars:
    letsencrypt_root: /var/www/html/laravel/public
    letsencrypt_domain: example.com
    letsencrypt_email: email@example.com
  roles:
    - { role: invokemedia.letsencrypt-nginx }
```

License
-------

MIT

Author Information
------------------

* [Invoke Media](http://www.invokemedia.com/)
* <biz@invokemedia.com>

References
----------

* [certbot installation docs](https://certbot.eff.org/#ubuntuxenial-nginx)
