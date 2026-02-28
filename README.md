sshfs_mount
===========

An Ansible role that installs and manages SSHFS mounts using systemd services.  
Supports both single-connection and multi-connection configurations via inventory variables.

Requirements
------------

This role requires:

- Linux system with systemd as init system
- Package manager support for installing `sshfs`
- SSH key-based authentication already configured between client and remote host
- Network connectivity to the SSHFS server
- Mount definitions should be placed in inventory variable files.

Role Variables
--------------
Define mounts in inventory host_vars or group_vars.

```yaml
sshfs_mounts:
  mount_name:
    user: string
    host: string
    remote_path: string
    local_path: string
    identity_file: string
```

Dependencies
------------
This role has no external Ansible role dependencies.

Author Information
-----
Author: MaathisV

Repository: https://github.com/MaathisV/ansible-role-sshfs-mount-service

If you use this role in production, please ensure private keys are stored securely using Ansible Vault or an external secret management system.