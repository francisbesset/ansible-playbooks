Ansible
=======

My ansible playbooks.

## Example usage

``` yaml
---
  - hosts: webservers

  - include: python/apt.yml
  - include: python/mysqldb.yml
  - include: dotdeb/dotdeb.yml with_php54=false
  - include: mysql/mysql.yml
    vars:
      mysqld:
        bind_address: 127.0.0.1
        key_buffer: 16M
        max_connection: 100
        # you can add other key/value
```
