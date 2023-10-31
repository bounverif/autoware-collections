ROS REQUIREMENTS INSTALL
=========

Downloads required packages to build and run ROS packages properly.

![Ansible Lint](https://github.com/bounverif/ansible-collection-ros/actions/workflows/ansible-lint.yml/badge.svg)

Requirements
------------

ROS2 must be installed on the system.

Role Variables
--------------

| Variable                | Required | Default      | Choices                   | Comments                                 |
|-------------------------|----------|--------------|---------------------------|------------------------------------------|
| ros_rmw_implementation  | yes      | `rmw_cyclonedds_cpp` | `rmw implementation string` | User must choose a rmw implementation file. Default one is provided as `rmw_cyclonedds_cpp`. |

Dependencies
------------

To run this role properly ROS2 must be installed on the system. Otherwise some packages may not be installed correctly.

Example Playbook
----------------

```
- name: Ros Requirements Install Role
  hosts: localhost
  connection: local
  vars:
    ros_rmw_implementation: rmw_cyclonedds_cpp
  roles:
    - role: bounverif.autoware_universe.ros_requirements_install
```

License
-------

See [license.md](https://github.com/bounverif/ansible-collection-ros/blob/main/LICENSE)

Author Information
------------------

https://github.com/bounverif/autoware-collections
