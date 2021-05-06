# macOS Developer Setup Using Ansible

This ansible playbook installs software to setup a dev environment via macOS, homebrew, and ansible.

Homebrew setup borrows heavily from https://github.com/adamchainz/mac-ansible.

## Assumptions

It is assumed that the following are available on your machine.

* bash
* curl

## Setup

To setup, run the setup script. This will install homebrew and then use that to install ansible.

```shell script
./setup.sh
```

## Install

Everything to be installed is listed in this [main.yaml](roles/development/tasks/main.yml).

Install is setup to be idempotent. If the software is already on the machine it will be skipped. Add software as you need it and re-use the script.

```shell script
./playbook-run.sh
```
