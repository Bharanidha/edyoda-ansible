# Directory structure

* To be aware of directory structure of role is essential to create and manage new role

* Roles have a structured layout

* The default structure can be changed if you wish to do so but for now lets stick with defaults

* You can create a role with any name and once it is created you can move it to folder roles for your identification

- tasks - contains the main list of tasks to be executed by the role.
- handlers - contains handlers, which may be used by this role or even anywhere outside this role.
- defaults - default variables for the role.
- vars - other variables for the role 
- files - contains files which can be deployed via this role.
- meta - defines some meta data for this role.
