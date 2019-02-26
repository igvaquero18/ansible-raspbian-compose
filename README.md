Raspbian Docker Compose
=========

This role installs [Docker Compose](https://docs.docker.com/compose/) on Raspbian operating systems as a container.

Requirements
------------

- Raspbian 9 (stretch) or later. It hasn't been tested with older versions, but that doesn't necessarily mean it can't work. Indeed, it should work with some older Raspbian versions.
- Pip

Role Variables
--------------

The only variable that can be set is:
- `raspbian_compose_version`: This tells which version of docker compose we want to install. By default it installs version 1.23.2, which is the latest at the time of writing.

Dependencies
------------

This role depends on the following:
- [igvaquero18.raspbian_docker](https://galaxy.ansible.com/igvaquero18/raspbian_docker)

Example Playbook
----------------

This is how you can add this role to your playbook

```yaml
- name: Install Docker Compose
  remote_user: ansible
  hosts: all
  roles:
    - {role: docker-compose, tags: [docker, compose]}
```

License
-------

BSD

Author Information
------------------

Ignacio Vaquero Guisasola.<br/>
DevOps Engineer at ING Spain.<br/>
[ivaqueroguisasola@gmail.com](mailto:ivaqueroguisasola@gmail.com).

