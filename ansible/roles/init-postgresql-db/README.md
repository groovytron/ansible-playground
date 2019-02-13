# Init PostgreSQL Database

Role allowing you to create a database on a PostgreSQL host.

## Requirements

Your server must have a running PostgreSQL service running. And a unix user able to use `psql` command and create databases and database users.

You also need to enable SSH pipelining to be able to use this user. Your `ansible.cfg` file should look like:

```cfg
[ssh_connection]
# Other SSH connection options...
pipelining = True
```

## Role Variables

You can override the following variables:

- `database_username`: The database user you want to create
- `database_name`: The name of the database you want to create
- `database_password`: The database user's password
- `database_encoding`: The database encoding

## Example Playbook

Use this role as the following:

```yaml
- hosts: all
  roles:
    - role: init-postgresql-db
      database_username: senty
      database_name: sentry
      database_password: sentry
  remote_user: postgresql
  become: yes
  become_method: sudo
```
