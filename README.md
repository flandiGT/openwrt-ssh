openwrt-ssh
===========

configure general aspects of your openwrt ssh.
see: [https://wiki.openwrt.org/doc/howto/dropbear.public-key.auth]

Role Variables
--------------

| variable name     | type                   | default                      |
|-------------------|------------------------|------------------------------|
| port              | port as number         | 22                           |
| password_auth     | boolean                | True                         |
| root_password_auth | boolean               | True                         |
| authorized_keys    | array of strings      | Array of ssh authorized keys |

Dependencies
------------

* python installed (at least in ram)

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
