* Tasks inside the block will be run first
* If there is a failure in any task in block, tasks inside rescue will be run
* The tasks inside always will always be run, whether or not there were failures in either block or rescue

* 0_playbook
- ignore unreachable host

* 1_playbook
- ignore_errors

* 2_ playbook
- failed_when

* 3_playbook
- rescue