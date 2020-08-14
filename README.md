[![License](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)

BeeGFS cluster Role
=======================

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows.
```

# Type of node to install: front or wn
type_of_node: front
# BeeGFS server host
server_host: '{{ hostvars[groups["front"][0]]["IM_NODE_PRIVATE_IP"] }}'
```

Example Playbook
----------------

This an example of how to install a SLURM cluster with three nodes:
```
- hosts: server
  roles:
  - { role: 'grycap.beegfs', type_of_node: 'front', main_beegfs_interface: 'eth1', server_host: '{{ hostvars[groups["front"][0]]["IM_NODE_PRIVATE_IP"] }}' }
```

