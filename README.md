ginhouxnet.packages
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
  - { name: bc, state: present } 
  - { name: ca-certificates, state: present }
  - { name: curl, state: present }
  - { name: dos2unix, state: present }
  - { name: ethtool, state: present }
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
