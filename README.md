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

| Platform | Versions |
|----------|----------|
| Debian | all |
| EL | all |
| Fedora | all |
| Ubuntu | all |

#### ANSIBLE VERSION

Ansible >= 2.13

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

#### EXAMPLES PLAYBOOKS

```yaml
- hosts: all
  roles:
    - name: Start role dginhoux.packages to setup "packages_list, packages_list_host and packages_list_group".
      vars:
        packages_action: setup
      ansible.builtin.include_role:
        name: dginhoux.packages
```

```yaml
- hosts: all
  roles:
    - name: Start role dginhoux.packages to check for availables upgrades
      vars:
        packages_action: check
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
# packages_action: setup


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

packages_list_host: []
packages_list_group: []
```

NOTE : Theses 3 lists `packages_list`, `packages_list_group` and `packages_list_host` are merged. <br />
You can use the host and group lists to specify users per host or group off hosts.



#### DEFAULT OS SPECIFIC VARIABLES

Those variables files are located in `vars/*.yml` are used to handle OS differences.<br />
One of theses is loaded dynamically during role runtime using the `include_vars` module and set OS specifics variable's.

`NOT USED BY THIS ROLE`



## AUTHOR

Dany GINHOUX - https://github.com/dginhoux



## LICENSE

MIT
