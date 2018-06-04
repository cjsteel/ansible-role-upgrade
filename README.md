# roles/upgrade/README.md

[![Build Status](https://travis-ci.org/cjsteel/upgrade.svg?branch=master)](https://travis-ci.org/cjsteel/upgrade)
[![Travis CI](http://img.shields.io/travis/csteel/upgrade/default.svg?style=flat)](http://travis-ci.org/csteel/upgrade/default)
[![Platforms](http://img.shields.io/badge/platforms-debian%20/%20ubuntu-lightgrey.svg?style=flat)](#)

## Description

upgrade is an Ansible role used to upgrade systems.

It is the equivalent of running something like the following from the command line:

```shell
# Upgrade all the CentOS systems.
ansible centos -m yum -a "name=* state=latest" -b

# Upgrade all the Debian systems
ansible debian -m apt -a "upgrade=yes update_cache=yes" -b

# Upgrade all the Fedora systemss.
ansible fedora -m dnf -a "name=* state=latest" -b

# Upgrade all the Ubuntu systems.
ansible ubuntu -m apt -a "upgrade=yes update_cache=yes" -b
```

## Recommended

Running Ansible in a virtual environment allows for a lot of testing flexibility.

* [docs/ansible-setup](docs/ansible-setup.md)

## Requirements

* Ansible

## Variables

### project_name/upgrade.yml

* [example_playbook.yml](files/example_playbook.yml)

To install:

```shell
cd project_directory
cp roles/upgrade/files/example_playbook.yml upgrade.yml
# edit if required
nano upgrade.yml
```

### project_name/site.yml

* [example_upgrade.yml](files/example_site.yml)

From the projects main directory run the following:

```yaml
cp roles/upgrade/files/example_playbook.yml upgrade.yml
cat upgrade.yml
```

### project/group_vars/all/project_defaults.yml

[files/group_vars/all/example_defaults.yml](files/group_vars/all/example_defaults.yml)

```yaml
cp roles/upgrade/files/group_vars/all/example_defaults.yml group_vars/all/project_defaults.yml
cat group_vars/all/project_defaults.yml
```

## Testing

Move into the role directory and run vagrant:

```shell
cd roles/upgrade
vagrant up
```

## Authors and License

- [Christopher Steel](http://mcin-cnim.ca/) | [e-mail](mailto:christopher.steel@mcgill.ca)
- [John Le](http://mcin-cnim.ca/) | [e-mail](mailto:john.le@mcgill.ca)
- [Andy Teng](http://mcin-cnim.ca/) | [e-mail](xiaoqiu.teng@mcgill.ca)

License: [MIT](https://tldrlegal.com/license/mit-license)

***
## Open Science

The Neuro has adopted the principles of Open Science. We are inspired by the likes of the Allen Institute for Brain Science, the National Institutes of Health's Human Connectome project, and the Human Genome project. For additional information, please see [Open Science at the Neuro](https://www.mcgill.ca/neuro/open-science-0).

![neuro](imgs/mcin-neuro-logo.png)

  

* ansible-role-upgrade generated using [galaxy-role-skeleton](https://github.com/cjsteel/galaxy-role-skeleton)
