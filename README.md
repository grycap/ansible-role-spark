[![License](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)

Apache Spark Role
==================

Ansible role to install Apache Spark (http://spark.apache.org/). A recipe for EC3 is also available in the EC3 repo.

Example Playbook
----------------
```
  - hosts: server
  roles:
  - { role: 'grycap.spark'}
```
```
  - hosts: client
  roles:
  - { role: 'grycap.spark'}
```

Contributing to the role
========================
In order to keep the code clean, pushing changes to the master branch has been disabled. If you want to contribute, you have to create a branch, upload your changes and then create a pull request.  
Thanks