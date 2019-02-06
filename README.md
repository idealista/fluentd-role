![Logo](logo.gif)

[![Build Status](https://travis-ci.org/idealista/fluentd-role.svg?branch=master)](https://travis-ci.org/idealista/fluentd-role)
# Fluentd Ansible role

This ansible role installs fluent agent in a Debian environment.

- [Getting Started](#getting-started)
	- [Prerequisities](#prerequisities)
	- [Installing](#installing)
- [Usage](#usage)
- [Testing](#testing)
- [Built With](#built-with)
- [Versioning](#versioning)
- [Authors](#authors)
- [License](#license)
- [Contributing](#contributing)

## Getting Started

These instructions will get you a copy of the role for your Ansible playbook. Once launched, it will install a [fluentd](https://fluentd.io/) agent.

### Prerequisities

Ansible 2.2.1.0 version installed.
Inventory destination should be a Debian environment.

For testing purposes, [Molecule](https://molecule.readthedocs.io/) with [Vagrant](https://www.vagrantup.com/) as driver (with [landrush](https://github.com/vagrant-landrush/landrush) plugin) and [VirtualBox](https://www.virtualbox.org/) as provider.

### Installing

Create or add to your roles dependency file (e.g requirements.yml):

```
- src: idealista.fluentd-role
  version: 1.0.0
  name: fluentd
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

## Usage

Look to the [defaults](defaults/main.yml) properties file to see the possible configuration properties.

It is mandatory to include a fluent.conf, you could use the defined default path or override var.

## Testing

```sh
molecule test
```

## Built With

![Ansible](https://img.shields.io/badge/ansible-2.2.1.0-green.svg)

## Versioning

For the versions available, see the [tags on this repository](https://github.com/idealista/fluentd-role/tags).

Additionaly you can see what change in each version in the [CHANGELOG.md](CHANGELOG.md) file.

## Authors

* **Idealista** - *Work with* - [idealista](https://github.com/idealista)

See also the list of [contributors](https://github.com/idealista/fluentd-role/contributors) who participated in this project.

## License

![Apache 2.0 License](https://img.shields.io/hexpm/l/plug.svg)

This project is licensed under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) license - see the [LICENSE](LICENSE) file for details.

## Contributing

Please read [CONTRIBUTING.md](.github/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.
