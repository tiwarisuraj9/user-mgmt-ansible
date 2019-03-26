# User mgmt. on multiple servers. ( Access/Revoke )

This is ansible playbook for giving access or to revoke access of multiple servers for dev users 


## Playbook-
`dev_users.yml` file contains list of dev users for which we will grant or revoke access on multiple servers.
`hosts` file contains IP's of all target servers


## How to deploy

This is how you would deploy all users.

```console
ansible-playbook -i hosts dev_users.yml -u ubuntu