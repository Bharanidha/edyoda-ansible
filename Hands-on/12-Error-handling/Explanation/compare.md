# Playbook without block

---
 - hosts: localhost
   gather_facts: no
   tasks:
    - command: "ls /home/localadmin/apache7"
      register: apache7_files
    - debug: var=apache7_files.stdout_lines
    - command: "ls /home/localadmin/apache8"
      register: apache8_files
    - debug: var=apache8_files.stdout_lines
    - command: "ls /home/localadmin/apache9"
      register: apache9_files
    - debug: var=apache9_files.stdout_lines


# Playbook with blocks

 ---
- hosts: localhost
  gather_facts: no
  tasks:
   - block:
      - command: "ls /home/localadmin/apache7"
        register: apache7_files
      - command: "ls /home/localadmin/apache8"
        register: apache8_files
      - command: "ls /home/localadmin/apache9"
        register: apache9_files
     ignore_errors: yes
