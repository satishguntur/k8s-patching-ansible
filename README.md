To ensure that the worker nodes only get patched after all the master nodes have been patched, you can structure your playbook into two separate plays, one for the masters and one for the workers. 
This way, the playbook will complete all tasks for the master nodes before starting on the worker nodes.

Here is the updated playbook:

Inventory File (hosts)
[masters]
master1
master2
master3

[workers]
worker1
worker2
worker3
worker4
worker5
worker6

run ansible playbook using ansible-playbook -i hosts main.yml
