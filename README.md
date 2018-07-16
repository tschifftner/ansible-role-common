# Ansible Role: Common

[![Build Status](https://travis-ci.org/tschifftner/ansible-role-common.svg?branch=master)](https://travis-ci.org/tschifftner/ansible-role-common)

Installs common packages on Debian/Ubuntu linux servers.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
common_packages:
  - haveged
  - curl
  - git
  - zip
  - unzip
  - vim
  - logrotate
  - nano
  - python-pip
  - wget
  - tar
  - pbzip2
  - bzip2
  - mc
  - bash-completion
  - mosh
  - hdparm
  - htop
  - iptraf
  - iftop
  - iotop
  - ncftp
  - screen
  - dnsutils
```

Define locale with:

```
common_locale: 'de_DE.UTF-8'

common_local_apt_packages:
  - locales
  - language-pack-en
  - language-pack-de

common_locale_generate_languages:
  - en_US.UTF-8
  - de_DE.UTF-8
```


## Dependencies

None.

## Example Playbook

    - hosts: server
      roles:
        - { role: tschifftner.common }

## Supported OS

 - Debian 9 (Stretch)
 - Debian 8 (Jessie)
 - Ubuntu 18.04 (Bionic Beaver)
 - Ubuntu 16.04 (Xenial Xerus)
 
## Required ansible version

Ansible 2.5+

## License

[MIT License](http://choosealicense.com/licenses/mit/)

## Author Information

 - [Tobias Schifftner](https://twitter.com/tschifftner), [ambimax® GmbH](https://www.ambimax.de)