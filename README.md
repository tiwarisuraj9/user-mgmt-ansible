# User mgmt. on multiple servers. ( Access/Revoke SSH)

This is ansible playbook for giving access or to revoke access of user for multiple servers


## Playbook-
`dev_users.yml` file contains list of dev users for which we will grant or revoke access on multiple servers.
`hosts` file contains IP's of all target servers


## How to deploy

This is how you would deploy all users.

***Target hosts are Ubuntu debian having python-minimal installed. This playbook only add SSh key and remove that particular key by giving below value of key `state`:-

***`state: present` to give access to user on all servers.

***`state: absent` to revoke access of particular user from all servers.

```console
ansible-playbook -i hosts dev_users.yml -u ubuntu
