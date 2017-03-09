# Jetstream Machine Ansible playbooks

This is currently a simple set of playbooks to create a single virtual machine in Jetstream.

it should work via

`ansible-playbook pga_host.yml`
 
I don't have the file 'clouds.yaml' included in this public repo, which is a necessity. 

It is equivalent to the openrc.sh - may be included later as a vault.

The basic format looks like:

```
clouds:
 tacc:
  auth: 
   username: value
   auth_url: value
   project_name: value
   password: value 
  user_domain_name: value
  project_domain_name: value
  identity_api_version: 3
```

Now with dynamic inventory (openstack.py).

The variables and hosts have been pulled from the main set of 
ansible playbooks in 

airavata/dev-tools/ansible

because some of the pga-config depends on other hosts. 

As more per-host playbooks are added, these can be removed. 

The pga role was also directly copied from the main ansible script 
location, to demonstrate a single-command build of the pga from
absolute scratch,  with dynamic inventory.
No more manual instance creation!

The complete build can be run via:
`ansible-playbook -i inventory pga_build.yml`
