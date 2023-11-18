# Домашнее задание к занятию 7 «Жизненный цикл ПО»

## Подготовка к выполнению

1. Получить бесплатную версию [Jira](https://www.atlassian.com/ru/software/jira/free).
2. Настроить её для своей команды разработки.
3. Создать доски Kanban и Scrum.

## Основная часть

Необходимо создать собственные workflow для двух типов задач: bug и остальные типы задач. Задачи типа bug должны проходить жизненный цикл:

1. Open -> On reproduce.
2. On reproduce -> Open, Done reproduce.
3. Done reproduce -> On fix.
4. On fix -> On reproduce, Done fix.
5. Done fix -> On test.
6. On test -> On fix, Done.
7. Done -> Closed, Open.

Остальные задачи должны проходить по упрощённому workflow:

1. Open -> On develop.
2. On develop -> Open, Done develop.
3. Done develop -> On test.
4. On test -> On develop, Done.
5. Done -> Closed, Open.

![image](https://github.com/Midzaru2011/mnt-homeworks/assets/102572340/421abfc3-7c87-4cd7-aeb3-461436fe7ead)
![image](https://github.com/Midzaru2011/mnt-homeworks/assets/102572340/02cfa765-b147-4077-befa-b59ccf48953d)

**Что нужно сделать**

1. Создайте задачу с типом bug, попытайтесь провести его по всему workflow до Done. 
2. Создайте задачу с типом epic, к ней привяжите несколько задач с типом task, проведите их по всему workflow до Done. 
3. При проведении обеих задач по статусам используйте kanban.
   ![image](https://github.com/Midzaru2011/mnt-homeworks/assets/102572340/480fd930-451e-4146-80bd-3abdda39e625)

4. Верните задачи в статус Open.
5. Перейдите в Scrum, запланируйте новый спринт, состоящий из задач эпика и одного бага, стартуйте спринт, проведите задачи до состояния Closed. Закройте спринт.
   ![image](https://github.com/Midzaru2011/mnt-homeworks/assets/102572340/345c6e39-6d1a-47b1-8117-802542aa2aec)

6. Если всё отработалось в рамках ожидания — выгрузите схемы workflow для импорта в XML. Файлы с workflow и скриншоты workflow приложите к решению задания.

[all task workflow.xml](https://github.com/Midzaru2011/mnt-homeworks/blob/main/09-ci-01-intro/all%20task%20workflow%20(1))

[bud workflow.xml](https://github.com/Midzaru2011/mnt-homeworks/blob/main/09-ci-01-intro/bug%20workflow%20(1).xml)
