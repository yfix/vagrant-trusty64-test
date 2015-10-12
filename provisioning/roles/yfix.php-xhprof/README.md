# Ansible Role: PHP-XHProf

[![Build Status](https://travis-ci.org/yfix/ansible-role-php-xhprof.svg?branch=master)](https://travis-ci.org/yfix/ansible-role-php-xhprof)

Installs PHP [XHProf](http://php.net/manual/en/book.xhprof.php) on Linux servers.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    TODO

## Dependencies

  - yfix.php
  - yfix.php-pecl

## Example Playbook

    - hosts: webservers
      roles:
        - { role: yfix.php-xdebug }
