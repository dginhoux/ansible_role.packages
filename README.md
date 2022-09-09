Ansible Role : dginhoux.packages
=========

This ansible role manage linux packages.
It can be used for : 
* install and remove packages
* check for update
* upgrades packages
* clean cache
* autoremove


Requirements
------------

This role is built to only run on platforms defined in `meta/main.yml`


Role Variables
--------------

Necessary variables are defined on `defaults/main.yml`

```yaml
# packages_action: upgrade
packages_action: check
# packages_action: autoremove
# packages_action: clean
# packages_action: install


packages_update_cache: yes


packages_list:
  - { name: fio, state: present }
  - { name: git, state: present }
  - { name: gitui, state: present, apt_ignore: yes }
  - { name: gpg, state: present }
  - { name: htop, state: present }
  - { name: haveged, state: present }
  - { name: hwinfo, state: present }
  - { name: iftop, state: present }
  # - { name: ifupdown2, apt: ifupdown2, dnf_ignore: yes, yum_ignore: yes }
  - { name: iotop, state: present }
  - { name: jq, state: present }
  - { name: lshw, state: present }
  - { name: lynx, state: present }
  - { name: lvm2, state: present }
  - { name: nfs, state: present, apt: nfs-common, dnf: nfs-utils, yum: nfs-utils }
  - { name: ngrep, state: present }
  - { name: nmon, state: present }
  - { name: nmap, state: present }
  - { name: oathtool, state: present }
  - { name: parted, state: present }
  - { name: python-apt, state: present, apt: python-apt, dnf_ignore: yes, yum_ignore: yes }
  - { name: python3-pip, state: present }
  - { name: python3-virtualenv, state: present }
  - { name: rsync, state: present }
  - { name: screen, state: present }
  - { name: scdaemon, state: present, dnf_ignore: yes, yum_ignore: yes }
  - { name: sshpass, state: present }
  - { name: sudo, state: present }
  - { name: sysstat, state: present }
  - { name: tig, state: present }
  - { name: tmux, state: present }
  - { name: tree, state: present }
  - { name: unzip, state: present }
  - { name: vim, state: present }
  - { name: yamllint, state: present }
  - { name: wget, state: present }
```


Dependencies
------------

none


Example Playbook
----------------



License
-------

BSD


Author Information
------------------

https://github.com/dginhoux/
