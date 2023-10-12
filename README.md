Ansible Role: Ubuntu Base VM
=========

An Ansible role to prepare an base VM template.

Requirements
------------

None.

Role Variables
--------------

You can select some apt and pip packages to install, what Github username to apply chezmoi dotfiles from, as well as wether to enable VMware customization scripts or not.

```yml
base_packages:
  - acl
  - bash-completion
  - ca-certificates
  - cifs-utils
  - curl
  - dialog
  - git
  - jq
  - mlocate
  - nano
  - neovim
  - net-tools
  - nfs-common
  - p7zip-full
  - python3
  - python3-pip
  - screen
  - smbclient
  - tmux
  - tree
  - unzip
  - vim
  - wget
  - whois
pip_packages:
  - pywinrm
  - pypsrp
  - requests
  - requests-credssp
  - github3.py
  - netaddr
  - dnspython
  - pyvmomi
  - argcomplete
chezmoi_user: xbufu
enable_vmware_customizations: true
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
- hosts: servers
  roles:
    - role: xbufu.ubuntu_base_vm
      vars:
        chezmoi_user: xbufu
        enable_vmware_customizations: true
```

License
-------

MIT / BSD

Author Information
------------------

Created by xbufu.
