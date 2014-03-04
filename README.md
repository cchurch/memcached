memcached
=========

This role installs a memcached server on the target host.

Requirements
------------

This role requires Ansible 1.4 or higher, and platform requirements are listed
in the metadata file.

Role Variables
--------------

The variables that can be passed to this role and a brief description about
each are as follows:

	memcached_host: 127.0.0.1       # The host/IP on which memcached server should be listening
	memcached_port: 11211           # The port on which memcached server should be listening
	memcached_max_conn: 1024        # The number of max concurrent connections it shoud accept
	memcached_cache_size: 64        # The cache size
	memcached_fs_file_max: 756024   # The kernel paramter for max number of file handles
	memcached_options: "-v"         # Extra command line options for memcached

Example
-------

The following play configures memcached with a different port number and
available memory.

	- hosts: all
	  sudo: true
	  roles:
	  - {role: cchurch.memcached, memcached_port: 11244, memcached_cache_size: 512 }


Testing
-------

Run "vagrant up" to create the defined VMs in the Vagrantfile and to provision the ```memcached.yml``` playbook, which imports this role.

At the moment, there are defined the following boxes:

* ```debian-720```: Debian 7.2.0 from Chef's Bento project.
* ```ubuntu-1204```: Ubuntu 12.04 from Chef's Bento project.

More boxes can be added by adding a new entry in the ```boxes``` array in the Vagrantfile. No other change should be necessary.

Dependencies
------------

None

License
-------

BSD

Author Information
------------------

Chris Church (forked from Benno Joy)
