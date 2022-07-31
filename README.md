# Ansible role: ansible_role_XYZ
[![CI](https://github.com/origox/ansible_role_XYZ/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/origox/ansible_role_XYZ/actions/workflows/ci.yml)

An Ansible role that install and configure XYZ

## Intial Setup after using template repo

1. Perform initial setup after using this template repo

Run from cmdline `grep -irl XYZ --exclude-dir=venv . | xargs sed -i 's/XYZ/git/gI'`
Note, replace NAME_OF_ROLE with your new name of Ansible role

2. Update tasks for actual configuration of new role.
3. Add needed directories
   - templates # i.e. jinja templates
   - meta, vars, ... 
4. Adapt readme file to new role 
5. Remove this chapter since it belongs only to creation phase of a new role. 

## Development and local test of new role
```bash
# Setup virtual environment
$ python3 -m pip install venv
$ source venv/bin/activate
$ python3 -m pip install -r requirements.txt

# YAML Lint
$ yamllint .

# Ansible lint
$ ansible-lint

# Molecule
$ molecule test
```

## Requirements

None.

## Role Default Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    XYZ_config:
      <section>:
        <key>: <value>

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - role: 
            src: https://github.com/origox/ansible_role_XYZ 
