puppet
======

Run puppet consistently from ansible.

Requirements
------------

puppet needs to be installed on the target node, and if puppet agent is being
used, the cert exchange needs to have been performed.

Role Variables
--------------

puppetmaster is the required parameter.

Dependencies
------------

None

Example Playbook
----------------

The only required argument is puppetmaster:

    - hosts: servers
      roles:
         - { role: infra.puppet, puppetmaster: puppetmaster.openstack.org }

License
-------

Apache

Author Information
------------------

ansible-puppet is maintained by the OpenStack Infra team. The best way to
contact them is on #openstack-infra on freenode.
