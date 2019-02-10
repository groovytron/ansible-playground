# Ansible playground

This repo contains a few experiments with Ansible. You can test is with
a virtual machine using `vargrant`.

## Requirements

The following softwares need to be installed on your machine:

- `vagrant`
- `ansible`
- machine virtualistion solution:
  - `libvirt/KVM` if you are one Linux and want a light solution
  - `virtualbox` if you are on OSX or Windows or you are on Linux don't feel
    comfortable with using `libvirt`

## Run the playbook on the Vagrant machine

You simply run the machine and the ansible playbook by running
`vagrant up --provider=<your-provider>` where `<your-provider>` is
the virtualization solution you chos to use (either `virtualbox` or
`libvirt`).

You can then ssh into the machine by running `vagrant ssh` from
the project's folder.

To stop the machine withtout destroying it run `vagrant halt` from
the project's folder.

To destroy the machine run `vagrant destroy` from the project's folder.

## What is happening

Vargant starts the machine (a Debian Jessie) and executes the playbook file
located in `ansible/playbook.yml` which uses the role `common` implemented in
`ansible/roles/common`. For more details about what this role does have a look
at the README in `ansible/roles/common/README.md`.
