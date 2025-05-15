# Initialization stand-alone server on Ubuntu 24 (noble)

[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](https://github.com/dafneb/.github/blob/main/.github/CODE_OF_CONDUCT.md)
[![License](https://img.shields.io/badge/License-MIT-4baaaa.svg)](https://github.com/dafneb/.github/blob/main/LICENSE)
![GitHub Release](https://img.shields.io/github/v/release/dafneb/ansible-role-ubuntu24-sa-server-init)
![GitHub commit activity](https://img.shields.io/github/commit-activity/w/dafneb/ansible-role-ubuntu24-sa-server-init)
![GitHub contributors](https://img.shields.io/github/contributors/dafneb/ansible-role-ubuntu24-sa-server-init)

![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/dafneb/ansible-role-ubuntu24-sa-server-init/ansible-lint.yml?label=ansible-lint)
![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/dafneb/ansible-role-ubuntu24-sa-server-init/codeql.yml?label=CodeQL)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/dafneb/ansible-role-ubuntu24-sa-server-init/badge)](https://scorecard.dev/viewer/?uri=github.com/dafneb/ansible-role-ubuntu24-sa-server-init)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/dafneb/ansible-role-ubuntu24-sa-server-init/main.svg)](https://results.pre-commit.ci/latest/github/dafneb/ansible-role-ubuntu24-sa-server-init/main)

An Ansible role to initial setup of stand-alone Ubuntu 24 server.

Adjusted settings:
- disabling cloud-init
- update of packages via apt
- adjusting message of the day
- adjusting local login warning banner
- adjusting remote login warning banner
- adjusting timezone
- adjusting NTP client (timesyncd, chrony)

## Requirements

No special requirements. Some tasks require "privileged role" at system. So, use [become](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_privilege_escalation.html#using-become) option at your inventory list.

## Role Variables

This role is designed so the end user should not have to edit the tasks themselves. All customizing should be done via the defaults/main.yml file or with extra vars within the project, job, workflow, etc.

## Example Playbook

    - hosts: servers
      roles:
         - { role: dafneb.ubuntu24-sa-server-init }

## License

[MIT](LICENSE)
