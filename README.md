# ansible-role-git

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-git.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-git)

RHEL/CentOS - Check-out git repositories

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    git_packages: [ 'git-all' ]
    git_repos: ''

You can clone multiple repositories by doing the following:

    git_repos:
      ansible-role-dome9:
        dst: "{{ ansible_env.HOME }}/ansible-role-dome9"
        org: linuxhq
        server: github.com
      ansible-role-dome9agent:
        dst: "{{ ansible_env.HOME }}/ansible-role-dome9agent"
        org: linuxhq
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

BSD

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).