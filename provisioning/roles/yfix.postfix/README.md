# Ansible Role: Postfix

[![Build Status](https://travis-ci.org/yfix/ansible-role-postfix.svg?branch=master)](https://travis-ci.org/yfix/ansible-role-postfix)

Installs postfix on RedHat/CentOS or Debian/Ubuntu.

## Requirements

If you're using this as an SMTP relay server, you will need to do that on your own, and open TCP port 25 in your server firewall.

## Role Variables

None.

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - { role: yfix.postfix }
