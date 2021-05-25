# openstack horizon


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


Test
----

    [user@localhost openstack-horizon]$ molecule converge
    [user@localhost openstack-horizon]$ podman ps
    CONTAINER ID  IMAGE                        COMMAND               CREATED        STATUS            PORTS   NAMES
    46ceeb4a8b5d  docker.io/pycontribs/ubuntu  bash -c while tru...  3 minutes ago  Up 3 minutes ago    instance
    [user@localhost openstack-horizon]$ molecule login
    [root@712c7b4ac78c /]# whoami
    root
    [root@712c7b4ac78c /]# exit
    [user@localhost openstack-horizon]$ molecule destroy

