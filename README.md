[![License](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)

BeeGFS cluster Role
=======================

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows.
```

# Type of node to install: front or wn
vnode_prefix: front
# Class to use as power manager (POWERMANAGER_CLASS)
clues_powermanager_class: cluesplugins.im
```

Example Playbook
----------------

This an example of how to install a SLURM cluster with three nodes:
```
- hosts: server
  roles:
  - { role: 'grycap.beegfs', vnode_prefix: 'front'}
```

