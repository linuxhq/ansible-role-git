# ansible-role-git

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-git.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-git)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-git-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/git)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

Linux - Clone git repositories

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    git_packages:
      - git-all
    git_repos: {}

You can clone multiple repositories by doing the following (protocol defaults to https):

    git_repos:
      ansible-role-dome9:
        dst: "{{ ansible_env.HOME }}/ansible-role-dome9"
        org: linuxhq
        protocol: ssh
        server: github.com
      ansible-role-dome9agent:
        dst: "{{ ansible_env.HOME }}/ansible-role-dome9agent"
        org: linuxhq
        protocol: git
        server: github.com

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.git
          git_packages:
            - git
            - git-svn

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
