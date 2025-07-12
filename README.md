UFW Role
=========

This role aims to manage basic firewall using ufw

Requirements
------------

Using a debian based distro supporting `ufw` package

Role Variables
--------------

UFW configuration structure:
'''
ufw_rules:
  input:
    default_policy: "deny"
    rules:
  output:
    default_policy: "allow"
    rules: []
```

Rule structure:
```
- comment: ""
  src_hosts: []
  dst_ports: []
  src_ports: []
  dst_hosts: []
```

Dependencies
------------

**None**

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:


```
ufw_rules:
  input:
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
  output:
    default_policy: "allow"
    rules: []
```

License
-------

MIT

Author Information
------------------

* stethewwolf

