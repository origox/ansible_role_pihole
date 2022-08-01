# Ansible role: ansible_role_pihole
[![CI](https://github.com/origox/ansible_role_pihole/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/origox/ansible_role_pihole/actions/workflows/ci.yml)

An Ansible role that install and configure pihole

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

    pihole_config:
      <section>:
        <key>: <value>

## Dependencies

## Misc
How to generate password - echo -n mypassword | sha256sum | awk '{printf "%s",$1 }' | sha256sum

None.

## Example Playbook

    - hosts: all
      roles:
        - role: 
            src: https://github.com/origox/ansible_role_pihole 
