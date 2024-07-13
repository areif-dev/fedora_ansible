# Personal Ansible Provisioning Tasks 

A playbook to quickly configure a Fedora desktop using the River tiling Wayland compositor and all my preferrences.

```bash
git clone https://github.com/areif-dev/ansible-provision -b <branch-name>
```

## Installing 

These playbooks are mostly designed to be run on the local system, rather than on a remote target. Therefore, first make sure that [https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#selecting-an-ansible-package-and-version-to-install](Ansible is installed). 

Now clone the repo with your preferred branch selected: 

```bash 
git clone -b fedora-desktop https://github.com/areif-dev/ansible-provision && cd ansible-provision
```

## Configuring vars.yml

The only input required from you is to copy the contents of `example_vars.yml` to `vars.yml` and replace the default values there with your preferrences. Currently, the only values that are in this file are the name of the `primary_user`, the path to the `preferred_shell`, the `hostname` of the system, and some options related to the speed of DNF.

## Running 

Once the repo is cloned and `vars.yml` has been created and configured, simply run 

```bash 
ansible-playbook local.yml
```

as root in the directory where `ansible-provision` was downloaded. 
