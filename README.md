# Ansible Role: OpenSSL Certs [Ansible Playbook Role To Install & Generate OpenSSL Certs]

Install & Generate OpenSSL Certs, on any RHEL/CentOS Linux system.

## Requirements

None.

## Role Variables
```yml


```

## Dependencies

None.

## Usage and Example Playbook

Install from Ansible Galaxy

$ ansible-galaxy install avinash6784.openssl-certs
Or download manually

$ git clone https://github.com/avinash6784/ansible-role-openssl-certs.git 
The code should reside in the roles directory of ansible ( See ansible documentation for more information on roles ), in a folder ansible-role-openssl-certs.

## Run the playbook

First create a playbook including the git role, naming it test.yml.
```yml
- name: Install OpenSSL Certs
  hosts: localhost
  become: true
  roles:
    - ansible-role-openssl-certs
    
$ ansible-playbook -i hosts test.yml
```

## Author Informations

This role was created by [Avinash Pawar](https://github.com/avinash6784/)
