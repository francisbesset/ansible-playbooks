Ansible
=======

My ansible playbooks.

## Example usage

``` yaml
---
  - hosts: webservers

    vars:
      # dotdeb
      with_php54: true

    tasks:
      - include: python/tasks/setup-apt.yml
      - include: dotdeb/tasks/setup.yml
```
