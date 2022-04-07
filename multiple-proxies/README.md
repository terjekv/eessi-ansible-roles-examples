# Multiple proxies and multiple client configurations

This example shows a site that has HPC nodes that use two proxies, other internal clients that use two other proxies, and a single proxy that for external users.

To achieve this setup without a lot of copy-paste, we use group variables for each of the different inventory groups, and we use inventory inheritance to abstract away the different type of proxies and clients, relying on the group variables to set the appropriate allowed client list for the proxies and proxy settings for the client.

To execute this example, update the inventory file and do:

````
ansible-galaxy install -r ../requirements.yml
ansible-playbook -i inventory site.yml
````