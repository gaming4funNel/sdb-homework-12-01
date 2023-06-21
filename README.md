# Домашнее задание к занятию «Базы данных» - Иванов Игорь

### Легенда

Заказчик передал вам [файл в формате Excel](https://github.com/netology-code/sdb-homeworks/blob/main/resources/hw-12-1.xlsx), в котором сформирован отчёт. 

На основе этого отчёта нужно выполнить следующие задания.

### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:

- какие данные хранятся в этих таблицах;
- какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

Приведите решение к следующему виду:

Сотрудники (

- идентификатор, первичный ключ, serial,
- фамилия varchar(50),
- ...
- идентификатор структурного подразделения, внешний ключ, integer).

employee (

- emp_id, первичный ключ, serial
- fio, varchar(50)
- date_from, date
- department_id, smallint, внешний ключ department (dep_id)
- position_id, smallint, внешний ключ position (pos_id)
- branch_id, smallint, внешний ключ branch (branch_id)
- current_project_id, smallint, внешний ключ projects (project_id)
- pos_salary, money, внешний ключ position (salary)).

department (

- dep_id, primary_key, serial
- dep_name, varchar(50)
- dep_type, smallint, внешний ключ deptypes (deptype_id)).

deptypes (
- deptype_id, первичный ключ, serial
- deptype_name, varchar(20)).

position (
- pos_id, первичный ключ, serial
- position_name, varchar(50)
- salary, money
- department_id, varchar(50), внешний ключ department (dep_id)).

branch (
- branch_id, первичный ключ, serial
- address_id, smallint, внешний ключ addresses (address_id)
- branch_endpoint, varchar (100)
- branch_regoin_id, smallint, внешний ключ addresses (address_area)).

addresses(
- address_id, первичный ключ, serial
- address_area, varchar(50)
- address_city, varchar(50)
- address_street, varchar(100)
- address_building, varchar (30)).

projects (
- project_id, первичный ключ, serial
- project_name, varchar(100)).

## Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже шире разобраться в материале.


### Задание 2*

Перечислите, какие, на ваш взгляд, в этой денормализованной таблице встречаются функциональные зависимости и какие правила вывода нужно применить, чтобы нормализовать данные.



