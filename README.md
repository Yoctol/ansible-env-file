Role Name
=========

Role to render env file with ease.

Requirements
------------

Ansible >= 1.2

Role Variables
--------------

```yaml
# Env object to make env file with.
env: {}

# Required, the path where dockerfile to be rendered on the host.
dest: ~/env-file

# Optional, the args of ansible template module except `src` and `dest`.
# Check http://docs.ansible.com/ansible/template_module.html.
template_options: {}
```


Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - role: env_file
      dest: ~/env-file
      template_options: owner=root mode=u=rw,g=r,o=r
```

License
-------

MIT

Author Information
------------------

Yoctol Info Inc.
