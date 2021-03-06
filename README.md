# Ansible basic VM setup CentOS 7

This repository contains a playbook for provisioning a base centOS machine.

## Features

* User setup
* SSH hardening (no password login, no root login)
* Firewall setup (HTTP/S and SSH allowed)
* Fail2Ban


## Usage

Configure your [hosts file](https://github.com/w-vi/ansible-base-centos/blob/master/hosts).

```
[production]
192.168.1.1 # example.com
```

and edit [provision.yml](https://github.com/w-vi/ansible-base-centos/blob/master/provision.yml)
to configure the non root user. This will create a new user on the
provisioned server that can be used later.

Execute:

```
$ ansible-playbook provision.yml
```

If the initial root user needs password:

```
$ ansible-playbook provision.yml --ask-pass
```
