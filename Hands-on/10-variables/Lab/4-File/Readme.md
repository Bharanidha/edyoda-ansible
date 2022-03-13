# Declaring variable in file

* It’s a great idea to keep playbooks under source control, but you may wish to keep certain important variables private

* Similarly, sometimes you may just want to keep certain information in different files

* This removes the risk of sharing sensitive data with others when sharing your playbook source with them

* We can use “vars_files” module to call this files.
