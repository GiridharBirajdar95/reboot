---
- name: Restart Server
  hosts: your_target_servers
  become: yes  # Run tasks with sudo (root) privileges

  tasks:
    - name: Restart the Server
      command: "reboot"
      async: 0
      poll: 0

