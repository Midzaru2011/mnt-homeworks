# Домашнее задание к занятию 4 «Работа с roles»

## Подготовка к выполнению

1. * Необязательно. Познакомьтесь с [LightHouse](https://youtu.be/ymlrNlaHzIY?t=929).
2. Создайте два пустых публичных репозитория в любом своём проекте: vector-role и lighthouse-role.
3. Добавьте публичную часть своего ключа к своему профилю на GitHub.

## Основная часть

Ваша цель — разбить ваш playbook на отдельные roles. 

Задача — сделать roles для ClickHouse, Vector и LightHouse и написать playbook для использования этих ролей. 

Ожидаемый результат — существуют три ваших репозитория: два с roles и один с playbook.

**Что нужно сделать**

1. Создайте в старой версии playbook файл `requirements.yml` и заполните его содержимым:

```---
  - src: https://github.com/Midzaru2011/clickhouse-role.git
    scm: git
    version: "1.0.0"
    name: clickhouse

  - src: https://github.com/Midzaru2011/lighthouse-role.git
    scm: git
    version: "1.0.1"
    name: lighthouse

  - src: https://github.com/Midzaru2011/vector-role.git
    scm: git
    version: "1.0.0"
    name: vector 
```

2. При помощи `ansible-galaxy` скачайте себе эту роль.

```shell
zag1988@mytest4:~/mnt-homeworks/08-ansible-04-role/playbook$ ansible-galaxy install -r requirements.yml -p roles
Starting galaxy role install process
- extracting clickhouse to /home/zag1988/mnt-homeworks/08-ansible-04-role/playbook/roles/clickhouse
- clickhouse (1.0.0) was installed successfully
- extracting lighthouse to /home/zag1988/mnt-homeworks/08-ansible-04-role/playbook/roles/lighthouse
- lighthouse (1.0.1) was installed successfully
- extracting vector to /home/zag1988/mnt-homeworks/08-ansible-04-role/playbook/roles/vector
- vector (1.0.0) was installed successfully
```

3. Создайте новый каталог с ролью при помощи `ansible-galaxy role init vector-role`.
4. На основе tasks из старого playbook заполните новую role. Разнесите переменные между `vars` и `default`. 
5. Перенести нужные шаблоны конфигов в `templates`.
6. Опишите в `README.md` роли и их параметры. Пример качественной документации ansible role [по ссылке](https://github.com/cloudalchemy/ansible-prometheus).

Роли:
> -  [Clickhouse] (https://github.com/Midzaru2011/clickhouse-role.git)
> -  [Lighthouse] (https://github.com/Midzaru2011/lighthouse-role.git)
> -  [Vector] (https://github.com/Midzaru2011/vector-role.git)

7. Повторите шаги 3–6 для LightHouse. Помните, что одна роль должна настраивать один продукт.
8. Выложите все roles в репозитории. Проставьте теги, используя семантическую нумерацию. Добавьте roles в `requirements.yml` в playbook.
9. Переработайте playbook на использование roles. Не забудьте про зависимости LightHols -luse и возможности совмещения `roles` с `tasks`.
10. Выложите playbook в репозиторий.

[Playbook](https://github.com/Midzaru2011/mnt-homeworks/blob/95edc8b303b22a03f87bd34043c5189c3cd5601b/08-ansible-04-role/playbook/site.yml)

11. В ответе дайте ссылки на репозитори с roles и одну ссылку на репозиторий с playbook.

[Vector-role](https://github.com/Midzaru2011/vector-role/tree/1.0.0)

[Lighthouse-role](https://github.com/Midzaru2011/lighthouse-role/tree/1.0.1)

[Clickhouse-role](https://github.com/Midzaru2011/clickhouse-role/tree/1.0.0)

---

### Как оформить решение задания

Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.

---
