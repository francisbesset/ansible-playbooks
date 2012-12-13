Ansible
=======

My ansible playbooks.

## Example usage

``` yaml
---
  - hosts: webservers

  - include: python/apt.yml
  - include: dotdeb/dotdeb.yml with_php54=false
```
