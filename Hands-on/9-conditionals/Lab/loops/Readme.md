# What are we doing with this playbook?

* Using this playbook we are creating loop based tasks.

* Sometimes you want to repeat a tasks multiple times. In computer programming, this is called a loop.

* Common use case of Ansible loops are

  - Changing ownership on several files and dictionaries with the file module.
  - Creating multiple users with user module.
  - Repeating a step until a certain result reached.

- To achive loop based tasks, ansible offers two modules `loop] and with_<lookup>`

* Note : Module loop can be used from Ansible version 2.5. 

* It’s not a complete replacement of <with_lookup> as it is still recommended to use most use cases

# Code explanation

* `playbook` 
   - This playbook helps to create loop based tasks.
   - If you are running this code from root user comment lines 3 & 4

# How to execute playbook?

 - Run playbook on hosts defined in inventory file (default)
   `ansible-playbook playbook_name.yml`

 - Running playbook by passing password
   root user password     : `ansible-playbook playbook_name.yml –k`
   non-root user password : `ansible-playbook playbook_name.yml –K`

 - Run Playbook on single host
   `ansible-playbook playbook_name.yml -i hostname1, hostname2`

 - Run Playbook on custom inventory file
   `ansible-playbook -i inventoryfilename playbook_name.yml`
   
 - Playbook Dry run
   `ansible-playbook playbook_name.yml –check`
