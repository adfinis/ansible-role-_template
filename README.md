# Ansible Role Template

This repository contains a template to generate an Ansible role. The generated role is an almost blank role.

Some opinions have been included to make a "working" example.

The only variable that is used is "role_name". This is the name you give when issuing

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

Now you can start coding, the advised order to modify files:

1. `README.md` - Describe the scope of your role.
2. `vars/main.yml` - Specify all packages, services, etc.
3. `defaults/main.yml` - Specify preferences for consumers of the role.

TODO: Finish this.
