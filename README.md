---
- name: Restart Server
  hosts: local hosts
  become: yes  # Run tasks with sudo (root) privileges

  tasks:
    - name: Restart the Server
      command: "reboot"
      async: 0
      poll: 0

