# nerve4-wazuh-indexer

An Ansible role that installs wazuh-indexer to Rhel Servers. More info about rkhunter: [link](https://wazuh.com/)


## Requirements

Make sure, you made your vars file with valid path to custom template or you can use Default vars.

You need `ansible 2.13.7` to run this module

## Tasks descriptions

- main.yml - Run the OS check and run the relevant playbook.
- add-rhel-repo.yml - Deploy repository on Rhel hosts.
- create-wazuh-certs.yml - Create wazuh certificates and store on local machine (!).
- rhel-install-wazuh-idx.yml - Deploy wqazuh-indexer on Rhel hosts.
- rhel-run-the-cluster.yml - Enable / Start service and run Cluster initialization.


## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
- hosts: servergroup
  become: true
  become_user: lee

  vars_files:
    - vars/main.yml
    
  roles:
    - nerve4-wazuh-indexer
```

## Maintainer Information
Lee | 2023