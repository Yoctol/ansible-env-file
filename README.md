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

# Optional template arguments, which are the args of template module except `src`.
# If not set, default template settings are used.
# Check http://docs.ansible.com/ansible/template_module.html.
owner:
group:
mode:
backup:
force:
validate:
selevel:
serole:
setype:
seuser:
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
