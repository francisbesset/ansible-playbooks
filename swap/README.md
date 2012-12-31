Swap
==========

## Swappiness

This playbook configure the swappiness.
See http://en.wikipedia.org/wiki/Swappiness for more informations

### Vars

* **swappiness**: The swappiness value (range 0 to 100)
    * Type: Integer
    * Default: 60

### Usage

``` bash
$ ansible-playbook swappiness.yml -uroot --extra-vars "swappiness=60"
```
