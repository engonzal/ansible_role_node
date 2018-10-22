### Ansible Roles: Node

Role to install the Node Version Manager and Nodejs

#### Role Variables
To install node under the ansible users directory (sudo not required):
```
node_version: v8.12.0
nvm_version: v0.33.11
```

Optionally change the user NVM installs as:
```
nvm_install_user: "{{ ansible_user_id }}"
```

#### Example Playbook

```
    - hosts: servers
      vars:
        package_list:
        - curl
        - htop
      roles:
         - { role: engonzal.ansible_role_node, tags: [ 'node'] }
```

#### License

BSD

#### Author

Noe Gonzalez - http://engonzal.com
