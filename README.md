# Example for using the EESSI ansible roles

This repository is an example of how to use https://github.com/terjekv/ansible-eessi-roles in your own environment. You may already have inventory files and nodes, or not, but hopefully this example repository will help you deploy EESSI with ansible to your nodes.

Before running these examples, update the inventory file in question and fetch the requirements:

````
ansible-galaxy install -r requirements.yml
````

The entire example configuration can then be run, in the directory in question like so:

````
cd single-site
ansible-playbook -i inventory site.yml
````

## Example 1, a single site unified setup

[This example](single-site/) sets up a site with:

1. One stratum1
2. Two proxies
3. Multiple clients that all connect to the same two proxies we have defined
   
## Example 2, a setup with multiple proxies and multiple client configurations

[This example](multiple-proxies/) sets up a site with:

1. One stratum1
2. Six proxies (two internal, two HPC, two public)
3. Multiple clients with different connection strategies.