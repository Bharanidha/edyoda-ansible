# Create simple role

* For example, create role in name of sample by using command.

`ansible-galaxy init sample`

It generates directories as follows:

├── README.md
├── defaults
│   └── main.yml – [default variables for the role]
├── files – [contains files which can be deployed via this role]
├── handlers
│   └── main.yml -  [contains handlers, which may be used by this role or even anywhere outside this role]
├── meta
│   └── main.yml – [defines some meta data for this role]
├── tasks
│   └── main.yml – [Contains the main list of tasks to be executed by the role]
└── vars
    └── main.yml – [Other variables for the role]