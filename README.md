# Ansible Role: OpenSSL Certs [Ansible Playbook Role To Install & Generate OpenSSL Certs]

Install & Generate OpenSSL Certs, on any RHEL/CentOS Linux system.

## Requirements

None.

## Role Variables
```yml

ssl_certs_country: "IN"
ssl_certs_locality: "Pune"
ssl_certs_organization: "DevOps Techie"
ssl_certs_state: "Maharashtra"
ssl_certs_common_name: "{{ansible_fqdn}}"
ssl_certs_days: "365"
ssl_certs_fields: "/C={{ssl_certs_country}}/ST={{ssl_certs_state}}/L={{ssl_certs_locality}}/O={{ssl_certs_organization}}/CN={{ssl_certs_common_name}}"

ssl_certs_path: "/etc/ssl/{{ssl_certs_common_name}}"
ssl_certs_path_owner: "ansible"
ssl_certs_path_group: "ansible"
ssl_certs_privkey_path: "{{ssl_certs_path}}/{{ssl_certs_common_name}}.key"
ssl_certs_cert_path: "{{ssl_certs_path}}/{{ssl_certs_common_name}}.pem"
ssl_certs_csr_path: "{{ssl_certs_path}}/{{ssl_certs_common_name}}.csr"
ssl_certs_dhparam_path: "{{ssl_certs_path}}/dhparam.pem"
ssl_certs_mode: "0700"
ssl_certs_force_replace: yes

ssl_certs_local_privkey_path: "{{inventory_dir|default(playbook_dir)}}/files/ssl/{{ssl_certs_common_name}}.key"
ssl_certs_local_cert_path: "{{inventory_dir|default(playbook_dir)}}/files/ssl/{{ssl_certs_common_name}}.pem"
ssl_certs_local_privkey_data: ""
ssl_certs_local_cert_data: ""

ssl_certs_generate_self_signed: true
ssl_certs_key_size: "2048"
ssl_certs_generate_dh_param: false
ssl_certs_dhparam_size: "2048"

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
