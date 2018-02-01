[![License](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)
[![Build Status](https://travis-ci.org/grycap/ansible-role-spark.svg?branch=master)](https://travis-ci.org/grycap/ansible-role-spark)

Apache Spark Role
==================

Ansible role to install Apache Spark (http://spark.apache.org/). A recipe for EC3 is also available in the EC3 repo.

Role Variables
--------------

The following variables can be passed to this role:

	# The version of Spark (default value: 1.6.3)
	spark_version: 2.2.1
	# List of servers to download the spark code
	spark_mirrors: [ "http://apache.rediris.es/spark", "http://apache.uvigo.es/spark", "http://www-eu.apache.org/dist/spark" ]
	# Frontend private IP
	front_private_ip: ""
	# Node type
	spark_type_of_node: "front"
	# Mesos variables
	principal: 'ubuntu'
	secret: 'ubuntusecret'


Example Playbook
----------------
```
  - hosts: server
    roles:
     - { role: 'grycap.spark', spark_version: '2.2.1', spark_type_of_node: 'front', front_private_ip: '192.168.xxx.xxx'}
```
```
  - hosts: client
    roles:
     - { role: 'grycap.spark', spark_version: '2.2.1', spark_type_of_node: "wn"}
```

Contributing to the role
========================
In order to keep the code clean, pushing changes to the master branch has been disabled. If you want to contribute, you have to create a branch, upload your changes and then create a pull request.  
Thanks
