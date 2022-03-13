* Tasks inside the block will be run first
* If there is a failure in any task in block, tasks inside rescue will be run
* The tasks inside always will always be run, whether or not there were failures in either block or rescue