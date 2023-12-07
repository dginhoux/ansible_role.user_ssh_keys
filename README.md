# ROLE dginhoux.user_ssh_key



## DESCRIPTION

This ansible role deploy (and remove) ssh keys files for users in their home folder.<br />
It just copy keys files from a local files folder. <br />
This source folder must be secured, in my case the folder is unsecure, but the controler is secured and very restricted.


## REQUIREMENTS

#### SUPPORTED PLATFORMS

This role is tested on the following platforms.<br />

| Platform | Versions |
|----------|----------|
| ArchLinux | all |
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
ansible-galaxy install dginhoux.user_ssh_key
```
#### GIT

```shell
git clone https://github.com/dginhoux/ansible_role.user_ssh_key dginhoux.user_ssh_key
```


## USAGE

#### EXAMPLE PLAYBOOK

```yaml
- hosts: all
  roles:
    - name: start role dginhoux.user_ssh_key
      ansible.builtin.include_role:
        name: dginhoux.user_ssh_key
```


## VARIABLES

#### DEFAULT VARIABLES

Default variables defined in `defaults/main.yml` : 
user_ssh_keys_list:
  - name: sample
    keys_folder: /home/sample/.ssh
    keys_files:
      - name: id_rsa
        state: present
        src_location: "files/sample"
```yaml




```
#### DEFAULT OS SPECIFIC VARIABLES

Those variables files are located in `vars/*.yml` are used to handle OS differences.<br />
One of theses is loaded dynamically during role runtime using the `include_vars` module and set OS specifics variable's.

`NOT USED BY THIS ROLE`

## AUTHOR

Dany GINHOUX - https://github.com/dginhoux



## LICENSE

MIT
