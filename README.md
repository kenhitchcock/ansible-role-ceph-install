Role Name
=========

name: ansible-role-ceph-install
The purpose of this role is to install ceph on the nodes specified. 

Requirements
------------

System is subscribed to Red Hat
All repo's are setup correctly 

Roles are available to do the above if required.

Role Variables
--------------

Most variables required for this role to run are currently set in the defaults directory of the role and dont need to be set. 

OpenShift Versioning variables. Default values set to the following already.
     ceph_version: 4


## Required variables
However you will need the following.




Example Playbook
----------------

- name: "Ceph Install playbook"
  hosts: ceph  
  become: true

  tasks:
    - name: "Build Ceph Cluster"
      include_role:
        name: ../roles/ansible-role-ceph-install


License
-------

MIT

