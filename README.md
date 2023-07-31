# Role Name

A brief description of the role goes here.

## Requirements

- [host system settings for running playbook, as well as settings for vscode](https://github.com/mmblsp/ansible_requirements)
- [settings vscode](https://github.com/ansible/vscode-ansible)

```json
{
    "ansible.python.interpreterPath": "<PATH FOR Python>",
    "ansible.validation.enabled": true,
    "ansible.ansible.path": "ansible",
    "ansible.validation.lint.enabled": true,
    "ansible.completion.provideModuleOptionAliases":true,
    "ansible.ansible.useFullyQualifiedCollectionNames": false
}
```

## Role Variables

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

## Dependencies

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

## Environment variables for molecules operation

To work with delegated drivers and ycc_vm modules, you need to install the module in the ansible environment and fill in the environment variables on the control machine

- [module-yandex-cloud](https://github.com/arenadata/ansible-module-yandex-cloud)

- Put modules in the directory

```sh
ansible-config dump |grep DEFAULT_MODULE_PATH
```

at the moment, the files are added directly to the role directory

- add a file .bashrc lines

```sh
export YCC_TOKEN='<TOKEN>'
export YCC_FOLDER_ID='<F_ID>'
export YCC_SUBNET_ID='<N_ID>'

```

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
- hosts: servers
  roles:
      - { role: username.rolename, x: 42 }
```

## License

MIT

## Author Information

- [all my projects](https://github.com/mmblsp)
- [my social network](https://vk.com/mmblspace)
