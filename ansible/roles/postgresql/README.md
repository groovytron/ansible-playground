# PostgreSQL Role

Role installing `PostgreSQL` on a machine.

## Example Playbook

```
- hosts: all
  roles:
    - postgresql
  vars:
    - additionnal_locales:
      - fr_CH.UTF-8
  remote_user: root
  become: yes
```
