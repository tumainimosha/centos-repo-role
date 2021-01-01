# Ansible Role: Enable Centos Repositories on RHEL Server

Installs the Centos repository for RHEL.

## Requirements

This role only is needed/runs on RHEL and its derivatives.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    centos_repo_url: "http://ftp.heanet.ie/pub/centos/{{ ansible_distribution_major_version }}/os/{{ ansible_userspace_architecture }}"
    centos_repo_gpg_key_url: "http://ftp.heanet.ie/pub/centos/{{ ansible_distribution_major_version }}/os/x86_64/RPM-GPG-KEY-CentOS-{{ ansible_distribution_major_version }}"

The Centos repo URL and GPG key URL. Generally, these should not be changed, but if this role is out of date, or if you need a very specific version, these can both be overridden.

    centos_repo_disable: false

Set to `true` to disable the Centos repo (even if already installed).

## Dependencies

None.

## Example Playbook

    - hosts: servers
      roles:
        - centos-repo-role

## License

MIT / BSD

## Author Information

This role was created in 2021 by [Tumaini Mosha](https://github.com/tumainimosha), based on a similar role for EPEL repos by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).
