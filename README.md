Bashrc
========

Install a nice bash profile

Installs this profile for the root user, the current user and
also as skeleton for future users created on this system.

Requirements
------------

Debian Bullseye / Bookworm with the package python-pycurl and python-software-properties installed.
Also, you need bash for this to be of any use.

Role Variables
--------------

You can specify which users will get a `.bashrc` written to their homedir.
By default this roles uses the Ansible SSH user.

    bashrc_users:
      - "{{ ansible_ssh_user }}"

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - f500.bash
         - f500.bashrc

Linting
-------
Github actions will check this role with ansible-lint. To run this locally, you will need to follow the following steps:

```bash
brew install ansible-lint
brew install yamllint
ansible-lint
```

to fix the linting errors, run:

```bash
ansible-lint --fix
```

License
-------

LGPL-3.0

Author Information
------------------

Jasper N. Brouwer, jasper@nerdsweide.nl

Ramon de la Fuente, ramon@delafuente.nl
