# ROLE dginhoux.packages



## DESCRIPTION

This ansible role manage linux packages.<br />
It can be used for : <br />
* install and remove packages
* check for update
* upgrades packages
* clean cache
* autoremove


## REQUIREMENTS

#### SUPPORTED PLATFORMS

This role require a supported platform.<br />
It will skip node with unsupported platform to avoid any compatibility problem.<br />
This behaviour can be bypassed by settings the following variable `asserts_bypass=True`.

| Platform | Versions |
|----------|----------|
| Debian | buster, bullseye |
| Fedora | 33, 34, 35, 36, 37 |
| EL | 7, 8 |

#### ANSIBLE VERSION

Ansible >= 2.12

#### DEPENDENCIES

None.



## INSTALLATION

#### ANSIBLE GALAXY

```shell
ansible-galaxy install dginhoux.packages
```
#### GIT

```shell
git clone https://github.com/dginhoux/ansible_role.packages dginhoux.packages
```


## USAGE

#### EXAMPLE PLAYBOOK

```yaml
- hosts: all
  roles:
    - name: start role dginhoux.packages
      ansible.builtin.include_role:
        name: dginhoux.packages
```


## VARIABLES

#### DEFAULT VARIABLES

Defaults variables defined in `defaults/main.yml` : 

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

#### DEFAULT OS SPECIFIC VARIABLES

Those variables files are located in `vars/*.yml` are used to handle OS differences.<br />
One of theses is loaded dynamically during role runtime using the `include_vars` module and set OS specifics variable's.

`NOT USED BY THIS ROLE`



## AUTHOR

Dany GINHOUX - https://github.com/dginhoux



## LICENSE

MIT
