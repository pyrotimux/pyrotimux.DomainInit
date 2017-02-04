DomainInit
=========

Initializing and populating windows domain.

Requirements
------------

WMF 5 (or powershell) on window box.

Role Variables
--------------
Please pass in the variable below. Example is shown below.
```
# users to be populated in domain.
users:
  - { name: 'ichiban', pass: 'ichiV@gran7' }
  - { name: 'niban', pass: 'niV@gran7' }
  - { name: 'sanban', pass: 'sanV@gran7'}
  - { name: 'yonban', pass: 'yonV@gran7'}
  
# admins to be promoted
admins: "ichiban, niban"

domainname: "pyro.testrealm.local"
domainnetbios: "pyro"
domainadmin_user: "pyro"
domainadmin_pass: "V@gran7"
safemodeadmin_user: "safepyro"
safemodeadmin_pass: "V@gran7"
```

Dependencies
------------

You need the library folder in your ansible directory. It has the dsc modules needed for the play to work.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
- hosts: all
  gather_facts: true
  roles:
     - domain_init
```

License
-------

MIT

Author Information
------------------

chaosmuskey@gmail.com
