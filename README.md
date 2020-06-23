[![Build Status](https://travis-ci.com/form3tech-oss/fluentd-role.svg?branch=master)](https://travis-ci.com/form3tech-oss/fluentd-role)

# Fluentd Ansible role

This ansible role installs fluent agent in a Debian environment.

- [Getting Started](#getting-started)
	- [Prerequisities](#prerequisities)
	- [Installing](#installing)

## Getting Started

These instructions will get you a copy of the role for your Ansible playbook. Once launched, it will install a [fluentd](https://fluentd.io/) agent.

### Prerequisities

Ansible 2.2.1.0 version installed.
Inventory destination should be a Debian environment.

For testing purposes, [Molecule](https://molecule.readthedocs.io/) with [Vagrant](https://www.vagrantup.com/) as driver (with [landrush](https://github.com/vagrant-landrush/landrush) plugin) and [VirtualBox](https://www.virtualbox.org/) as provider.

### Installing

Create or add to your roles dependency file (e.g requirements.yml):

```
- src: https://github.com/form3tech-oss/fluentd-role
  name: fluentd
  version: <commit hash or branch name>
```

Install the role with ansible-galaxy command:

```
ansible-galaxy install -p roles -r requirements.yml -f
```

Use in a playbook:

```
- hosts: someserver
  roles:
    - role: fluentd
```

[Original readme](README.md.idealista)