openwrt-ssh
===========

configure general aspects of your openwrt ssh.
see: [https://wiki.openwrt.org/doc/howto/dropbear.public-key.auth]

Role Variables
--------------

| variable name     | type                   | default                      |
|-------------------|------------------------|------------------------------|
| authorized_keys   | array of strings       | Array of ssh authorized keys |

Dependencies
------------

* python installed (at least in ram)

Example Playbook
----------------

```
- role: openwrt-ssh
  authorized_keys: [
    'ssh-rsa AsLni1gBzlYKyjM0Ho...4bXURWWQoZAAyic9diM user@computer'
  ]
```
