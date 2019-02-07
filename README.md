ansible role template to be used with ansible-galaxy.

To create a new role:
`ansible-galaxy init --role-skeleton /path/to/ansible-role-template  $rolename`

Or update your `.ansible.cfg` file with:
```
[galaxy]
role_skeleton = /path/to/ansible-role-template
```

Then simply fix the role specific stuff.
