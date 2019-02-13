# Base Role


A base role used to install a basic debian configuration with:

- `bash` and `bash-completion`
- `git`
- `htop`
- `tmux`
- `vim`
- `zsh`

This role automatically enables `en_US.UTF-8` locale which are needed by
some softwares such as `postgresql`, `python`, `gradle`, etc.

## Role Variables

Here are the variables used for this role:

- `additionnal_locales`: the locales you want to make available additionnaly to `en_US.UTF-8`.

## Example Playbook

Use this role by doing the following in your `playbook.yml`:

```yaml
- hosts: servers
  roles:
    - role: base
      additionnal_locales:
        - fr_CH.UTF-8
```
