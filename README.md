Enix/$ROLE for Ansible
=================

A role for deploying and configuring [$ROLE](http://$rolesite.com) and extensions on unix hosts using [Ansible](http://www.ansible.com/).


Requirements
------------

Supported targets:

- Ubuntu 12.04 "Precise Pangolin"
- Debian 8 "Jessie"
- RedHat EL / CentOS 6
- ...


Role Variables
--------------

This roles comes preloaded with almost every available default. You can override each one in your hosts/group vars, in your inventory, or in your play. See the annotated defaults in `defaults/main.yml` for help in configuration. All provided variables start with `$ROLE__`.

- `$ROLE__` - desc

Dependencies
------------

- None

Extra
-----

Available extensions (under a switch):

- Extension - `$ROLE_extension`
- ...

Callable tasks:

- `task`: ...


Usage
-----

Clone this repo into your roles directory:

    $ git clone https://gitlab.enix.org/ansible/ansible-$ROLE.git roles/$ROLE

Or use Ansible galaxy requirements.yml

And add it to your play's roles:

    - hosts: servers
      roles:
        - { $ROLE: username.rolename, x: 42 }


You can also use the role as a playbook. You will be asked which hosts to provision, and you can further configure the play by using `--extra-vars`.

    $ ansible-playbook -i inventory --extra-vars='{...}' main.yml


Still to do
-----------

- Write the role itself, for one


Changelog
---------

### 0.1

Initial version.

License
-------

BSD/GPL/Other

Author Information
------------------

your name <your.name@enix.fr> - http://www.enix.fr
