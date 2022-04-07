# A single site example for EESSI setup

This site has one stratum1 server, two proxies, and all clients connect to the same proxies. This setup requires your proxies to be available to all your clients, which may or may not be the case.

To execute this example, update the inventory file and do:

````
ansible-galaxy install -r ../requirements.yml
ansible-playbook -i inventory site.yml
````