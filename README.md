[![role](https://img.shields.io/ansible/role/55379)](https://galaxy.ansible.com/trallnag/tmux)
[![quality](https://img.shields.io/ansible/quality/55379)](https://galaxy.ansible.com/trallnag/tmux)
[![downloads](https://img.shields.io/ansible/role/d/55379?label=downloads)](https://galaxy.ansible.com/trallnag/tmux)

# Endlessh

Install tmux on Ubuntu.

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/tmux).

## Role Variables

```yaml
tmux_conf_template:
  type: str
  required: true
  description: >-
    File containing tmux config. Can be templated.

tmux_packages:
  type: list
  elements: str
  default: ["tmux", "xclip", "git"]
  description: >-
    Packages to install. Must contain `tmux`, `xclip`, and `git`.

tmux_tpm_version:
  type: str
  default: v3.0.0
  description: >-
    Version of the TPM.
```

## Example Playbook

```yaml
- name: Playbook
  hosts: myhost
  remote_user: myuser
  vars:
    rolespec_validate: true
  roles:
    - name: trallnag.tmux
      vars:
        tmux_conf_template: "{{ playbook_dir }}/files/trallnag.tmux/tmux.conf"
        tmux_tpm_version: 2afeff1529ec85d0c5ced5ece3714c2220b646a5
```

## Special Requirements

None.

## Special Dependencies

None.

## License

Apache-2.0

## Author Information

Trallnag
