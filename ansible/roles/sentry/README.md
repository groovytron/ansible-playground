# Sentry Role

A brief description of the role goes here.

## Requirements

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

## Role Variables

Sentry configuration can be configured through this variables:

- `sentry_venv_path`
- `sentry_config_path`
- `sentry_mail_backend`
- `sentry_mail_host`
- `sentry_mail_port`
- `sentry_mail_username`
- `sentry_mail_password`
- `sentry_mail_use_tls`
- `sentry_mail_from`
- `sentry_database_name`
- `sentry_database_user`
- `sentry_database_password`
- `sentry_database_host`
- `sentry_database_port`
- `sentry_redis_host`
- `sentry_redis_port`
- `sentry_web_port`
- `sentry_filestore_location`

## Dependencies

- `Python 2` (needed by Sentry)

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
- hosts: all
  roles:
     - sentry
```
