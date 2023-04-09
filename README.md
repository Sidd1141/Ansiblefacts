# Ansiblefacts
Ansible playbook for retrieving facts from a ansible target node/server

Ansible Facts

Ansible is a powerful configuration management and automation tool that allows you to manage infrastructure as code. One of its most useful features is the ability to gather system information from remote hosts using "facts."

Facts are key-value pairs that represent information about a system, such as the operating system, network interfaces, disk usage, and more. These facts can be used in Ansible playbooks to make decisions, conditionally execute tasks, or simply report information back to the user.


Gathering Facts

To gather facts about a remote host, you simply need to run an Ansible task that collects them. Ansible provides a built-in setup module that retrieves a wide range of facts about the target host.

code/playbook


---
- name: Gather Facts
  hosts: web_servers
  gather_facts: yes
  tasks:
    - name: Show Facts
      debug:
        var: ansible_facts


In this playbook, the setup module is implicitly called when gather_facts is set to yes. The debug task then prints out all of the gathered facts using the ansible_facts variable.


Conclusion

Facts are a powerful feature of Ansible that allow you to gather system information and use it in your playbooks. Whether you are using the built-in facts or defining your own custom facts, Ansible makes it easy to automate your infrastructure with confidence.

