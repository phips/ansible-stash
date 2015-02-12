Role Name
========

Install [Atlassian Stash](https://www.atlassian.com/software/stash)

Requirements
------------

* Git
* Java
* A backend database. See [supported Stash platforms](https://confluence.atlassian.com/display/STASH/Supported+platforms)

Role Variables
--------------

All defined in defaults, so overrideable:

      stash_version:   3.6.1
      stash_baseurl:   http://www.atlassian.com/software/stash/downloads/binary
      stash_installer: atlassian-stash-3.6.1.tar.gz
      stash_user:      stash
      # use postgresql or mysql
      stash_dbconnector: postgresql
      stash_tmp:       /var/tmp
      stash_installto: /opt
      stash_datadir:   /srv/stash-data

Dependencies
------------

roles/java

Example Playbook
-------------------------

    - hosts: stash_servers
      roles:
         - { role: stash }

License
-------

MIT/BSD

Author Information
------------------

Mark Phillips <mark@probably.co.uk>
http://probably.co.uk
