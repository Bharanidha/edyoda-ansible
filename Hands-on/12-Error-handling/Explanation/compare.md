# Playbook without block

---
 - hosts: localhost
   gather_facts: no
   tasks:
    - name: list files apache
      command: "ls /home/localadmin/apache7"
      register: apache7_files
      when: ansible_os_family == "RedHat"
    - name: Print files
      debug: var=apache7_files.stdout_lines
      when: ansible_os_family == "RedHat"


# Playbook with blocks

 ---
- hosts: localhost
  gather_facts: no
  tasks:
  - name: Apache configuration
   block:
      - command: "ls /home/localadmin/apache7"
        register: apache7_files
      - debug: 
        var=apache7_files.stdout_lines
    when: ansible_os_family == "RedHat"
