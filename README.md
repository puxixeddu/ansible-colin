

<h1 align="center">
  Cisco Stig:rocket:
</h1>


# cisco_stig

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
