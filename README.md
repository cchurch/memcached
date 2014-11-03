## memcached [![Build Status](https://travis-ci.org/Oefenweb/ansible-memcached.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-memcached) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-memcached-blue.svg)](https://galaxy.ansible.com/list#/roles/1354)

Set up a memcached server in Debian-like systems.

#### Requirements

None

#### Variables

 * `memcached_logfile` [default: `/var/log/memcached.log`]: Log output to
 * `memcached_host` [default: `127.0.0.1`]: The IP address on which the server should be listening
 * `memcached_port` [default: `11211`]: The port on which the server should be listening
 * `memcached_max_connections` [default: `1024`]: The number of max concurrent connections it should accept
 * `memcached_memory_cap` [default: `64`]: The memory cap
 * `memcached_fs_file_max` [default: `false`]: The system file descriptor limit
 * `memcached_net_ipv4_ip_local_port_range` [default: `false`]: The system IP port limits
 * `memcached_options` [default: `''`]: Extra command line options for memcached

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
  - memcached
```

#### License

BSD

#### Author Information

Mischa ter Smitten (based on work of Benno Joy and Chris Churc)

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-memcached/issues)!
