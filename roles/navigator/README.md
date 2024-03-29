# Ansible role - mto79.ansible.navigator

## Table of Contents

- [Ansible role - mto79.ansible.navigator](#ansible-role---mto79ansiblenavigator)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Role variables](#role-variables)
    - [Setup](#setup)
    - [Upstream](#upstream)
  - [Example Playbook](#example-playbook)

## [Requirements](#requirements)

- The minimum version of Ansible required is 2.12.0.
- The minimum version of Jinja template 2.11.3

## [Role variables](#role-variables)

### Setup

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |
|`ansible_navigator_setup_shell_init` | string | `""` | The shell init script to be added to the user's shell profile. |
|`ansible_navigator_setup_path` | string | `""` | The path to the directory where the ansible navigator will be installed. |
|`ansible_navigator_setup_packages` | list | `["python3", "python3-pip"]` | The list of packages to be installed. |

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

## [Example Playbook](#example-playbook)

Refer to the following example:

```yaml
    - hosts: "servers"
      roles:
        - role: "mto79.ansible.navigator"
          vars:
            __role_action: "setup"
          tags: ['ansible', 'ansible-navigator']
```
