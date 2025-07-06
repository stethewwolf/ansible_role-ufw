UFW Role
=========

This role aims to manage basic firewall using ufw

Requirements
------------

Using a debian based distro supporting `ufw` package

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:


```
ufw_rules:
  Input:
    default_policy: "deny"
    rules:
      - comment: "Allow SSH"
        src_ports: []
        dst_ports: [22]
        src_hosts: []
        dst_hosts: []
      - comment: "Allow HTTP from LAN"
        src_hosts: ["192.168.1.0/24"]
        dst_ports: [80]
        src_ports: []
        dst_hosts: []
  Output:
    default_policy: "allow"
    rules: []
```

License
-------

MIT

Author Information
------------------



An optional section for the role authors to include contact information, or a website (HTML is not allowed).
