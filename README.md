puppet
======

Run puppet consistently from ansible.

Requirements
------------

puppet needs to be installed on the target node, and if puppet agent is being
used, the cert exchange needs to have been performed.

Role Variables
--------------

Either puppetmaster or manifest should be supplied. If you are using puppet
agent, you want to supply puppetmaster. If you are using puppet apply, you
want to supply manifest.

Dependencies
------------

None

Example Playbook using a puppetmaster
-------------------------------------

The only required argument is puppetmaster:

    - hosts: servers
      roles:
         - { role: puppet, puppetmaster: puppetmaster.openstack.org }


Example Playbook without a puppetmaster
-------------------------------------

The only required argument is manifest:

    - hosts: servers
      roles:
         - { role: puppet, manifest: /opt/system-config/production/manifests/site.pp }


License
-------

Apache

Author Information
------------------

ansible-puppet is maintained by the OpenStack Infra team. The best way to
contact them is on #openstack-infra on freenode.
