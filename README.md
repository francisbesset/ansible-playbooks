Ansible
=======

My ansible playbooks.

## Example usage

``` yaml
---
  - hosts: webservers

  - include: python/apt.yml
  - include: dotdeb/dotdeb.yml with_php54=false
  - include: mysql/mysql.yml
    vars:
        mysqld:
            bind_address: 127.0.0.1
            key_buffer: 16M
```
