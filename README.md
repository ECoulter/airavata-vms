# Jetstream Machine Ansible playbooks

This is a simple playbook to create a single virtual machine in Jetstream.

it should work via

`ansible-playbook pga_host.yml`
 
I don't have the file 'clouds.yaml' included, which is a necessity. 

This is equivalent to the openrc.sh - may be included later as a vault.

The basic format looks like:

```
clouds:
 tacc:
  auth: 
   username: value
   auth\_url: value
   project\_name: value
   password: value 
  user\_domain\_name: value
  project\_domain\_name: value
  identity\_api\_version: 3
```

This does NOT yet have any slick inventory generation, though 
it's on the TODO list.
