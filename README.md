eNiXHosting.$ROLE
=================

A role for deploying and configuring [$ROLE](http://$rolesite.com) and extensions on unix hosts using [Ansible](http://www.ansible.com/).


Requirements
------------

Supported targets:

- Ubuntu 12.04 "Precise Pangolin"
- Ubuntu 14.04 "Trusty"
- Ubuntu 16.04 "Xenial"
- Debian 8 "Jessie"
- Debian 9 "Stretch"
- RedHat EL / CentOS 6
- RedHat EL / CentOS 7
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

    # $ROLE from eNiXHosting
    # private role
    - src: git+ssh://git@gitlab.enix.org/ansible/ansible-$ROLE.git
      name: $ROLE

    # public role
    - src: eNiXHosting.$ROLE
      name: $ROLE

And add it to your play's roles:

    - hosts: all
      roles:
        - role $ROLE:
            $ROLE__var: true

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

GPLv2

Author Information
------------------

$your $name <$your.$name@enix.fr> - http://www.enix.fr
