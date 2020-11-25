

<h1 align="center">
  Cisco Stig:
<code><img height="22" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/ansible.svg"></code>
<code><img height="22" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/cisco.svg"></code>
</h1>




![ansible-lint](https://github.com/colin-mccarthy/cisco_stig/workflows/ansible-lint/badge.svg)



```

- hosts: "changeme"
  gather_facts: no
  connection: ansible.netcommon.network_cli
  
  vars:
    ansible_network_os: cisco.ios.ios
    ansible_network_cli_ssh_type: libssh
    
  tasks:
  - name: run show version command
    ansible.netcommon.cli_command:
      command: show version

  - name: run show interface command
    ansible.netcommon.cli_command:
       command: show interfaces
       
 ```      
