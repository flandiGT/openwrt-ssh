openwrt-ssh
===========

configure general aspects of your openwrt ssh.
see: [https://wiki.openwrt.org/doc/howto/dropbear.public-key.auth]

Dependencies
------------

* [openwrt-uci](https://github.com/flandiGT/openwrt-uci)
* python installed (at least in ram)

Role Variables
--------------

| variable name     | type                   | default                      |
|-------------------|------------------------|------------------------------|
| port              | port as number         | 22                           |
| password_auth     | boolean                | True                         |
| root_password_auth | boolean               | True                         |
| authorized_keys    | array of strings      | Array of ssh authorized keys |

Example Playbook
----------------

```
- role: openwrt-ssh
  port: 22
  password_auth: True
  root_password_auth: True
  authorized_keys:
    - 'ssh-rsa AsLni1gBzlYKyjM0Ho...4bXURWWQoZAAyic9diM user@computer'

```

Official documentation:
* [OpenWRT Wiki / Dropbear Configuration](https://wiki.openwrt.org/doc/uci/dropbear)
* [OpenWRT Wiki / Dropbear public-key authentication HowTo](https://wiki.openwrt.org/doc/howto/dropbear.public-key.auth)
