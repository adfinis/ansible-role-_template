# Ansible Role Template

This repository contains a template to generate an Ansible role. The generated role is an almost blank role.

Some opinions have been included to make a "working" example.

The only variable that is used is "role_name". This is the name you give when issuing the `ansible-galaxy init` as described in the next section.

## Usage

To instantiate a new role:

```shell
cd ~
# Please git clone this repository first: `git clone ...`
# Make a role called "example". (Use the short name, not "ansible-role-example".)
ansible-galaxy init --role-skeleton=ansible-role-_template example
# It's nice to add "ansible-role-" to the name of the folder, this is optional.
mv example ansible-role-example
cd ansible-role-example
```

## Test

The created role can be tested immediately after creation, provided the target host is reachable 
via ssh without password. 

The created `tests/inventory` file contains only `localhost`, so you have to ensure that 

```shell
ssh localhost
```

works without password. In case you run `ssh` on a non standard port (i.e. you use `ssh -p 1234 localhost`, 
you should add the port number in the inventory file:

```
localhost:1234
```

You can now test the newly instantiate example role:

```shell
cd tests
ansible-playbook playbook.yml -i inventory
```

## Development

Now you can start coding, the advised order to modify files:

1. `README.md` - Describe the scope of your role.
2. `vars/main.yml` - Specify all packages, services, etc.
3. `defaults/main.yml` - Specify preferences for consumers of the role.

