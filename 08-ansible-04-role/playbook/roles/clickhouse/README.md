Clickhouse
=========

Данная роль предназначена для установки ПО Clickhouse.

Role Variables
--------------
| variables | description |
|--------|-----------|
| clickhouse_version | версия дистрибутива clickhouse |

Example Playbook
----------------
```
- name: Install Clickhouse
  hosts: clickhouse
  roles:
    - clickhouse
```


Author Information
------------------

Midzaru2011
