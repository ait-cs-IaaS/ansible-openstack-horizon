# Ansible Role: openstack-horizon


Configures Openstack [Horizon](https://docs.openstack.org/horizon/latest/).

Role Varibles
-------------

| Name | Default value | Description | Note |
|---   |---            |---          |---   |
| `horizon_host_name` | `localhost` | Hostname/IP address of the controller node ||


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: openstack-horizon, horizon_host_name: localhost }

