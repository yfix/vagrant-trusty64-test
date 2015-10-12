# Ansible Role: PHP PECL extensions

[![Build Status](https://travis-ci.org/yfix/ansible-role-php-pecl.svg?branch=master)](https://travis-ci.org/yfix/ansible-role-php-pecl)

Installs PHP PECL extensions on servers with PHP already installed.

## Requirements

PHP must already be installed on the server (along with the package `php-pear`), so the `pecl` command can be run.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    php_pecl_extensions: []

A list of extensions that should be installed via `pecl install`. If you'd like to have this role install extensions like XDebug, just add it in the list, like so:

    php_pecl_extensions:
      - xdebug

## Dependencies

  - yfix.php

## Example Playbook

    - hosts: webservers
      vars_files:
        - vars/main.yml
      roles:
        - { role: yfix.php-pecl }

*Inside `vars/main.yml`*:

    php_pecl_extensions:
      - xdebug
