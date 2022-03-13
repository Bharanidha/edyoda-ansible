# Roles

* In Ansible, the role is the primary mechanism for breaking a playbook into multiple files

* This actually simplifies writing complex playbooks and it makes them easier to reuse

* The breaking of playbook allows you to logically break the playbook into reusable components

* Note: Roles are not playbooks

* Roles are small functionality which can be independently used but have to be referred within playbook to have it applied in remote machines

* There is no way to directly execute a role

* To keep it simple – playbooks are the bridge between your Roles and Inventory file
