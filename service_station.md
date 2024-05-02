# Калявин Владислав Олегович, ИС22/9-1 #
Я создал бд "service station" на тему "СТО".
![бд СТО](img/STO.jpg)
## Описание Бд ##
**Таблица boxes**
*id: INTEGER (Primary Key, Autoincrement)* - уникальный идентификатор ящика
*name: varchar(255)* - название ящика
*specialization_id: INTEGER* - идентификатор специализации, связан с таблицей **specialization**
*employees_id: INTEGER* - идентификатор сотрудника, связан с таблицей **employees**
![Пример записей из таблицы **boxes**:](img/boxes.PNG)

**Таблица brand**
*id: INTEGER (Primary Key, Autoincrement)* - уникальный идентификатор бренда
*name: varchar(255)* - название бренда
*country_id: INTEGER* - идентификатор страны, связан с таблицей **country**
![Пример записей из таблицы **brand**:](img/brand.PNG)

**Таблица car**
*id: INTEGER (Primary Key, Autoincrement)* - уникальный идентификатор автомобиля
*fullname: varchar(255)* - полное название автомобиля
*country_id: INTEGER* - идентификатор страны, связан с таблицей **country**
*brand_id: INTEGER* - идентификатор бренда, связан с таблицей brand
![Пример записей из таблицы **car**:](img/car.PNG)

**Таблица clients**
*id: INTEGER (Primary Key, Autoincrement)* - уникальный идентификатор клиента
*car_id: INTEGER* - идентификатор автомобиля, связан с таблицей **car**
*fullname: VARCHAR(255)* - полное имя клиента
![Пример записей из таблицы **clients**:](img/clients.PNG)

**Таблица country**
*id: INTEGER (Primary Key, Autoincrement)* - уникальный идентификатор страны
*name: varchar(83)* - название страны
![Пример записей из таблицы **country** :](img/country.PNG)

**Таблица details**
*id: INTEGER (Primary Key, Autoincrement)* - уникальный идентификатор детали
*fullname: varchar(255)* - полное наименование детали
*country_id: INTEGER* - идентификатор страны, связан с таблицей **country**
*car_id: INTEGER* - идентификатор автомобиля, связан с таблицей **car**
*partscost: NUMERIC* - стоимость детали
![Пример записей из таблицы **details**:](img/details.PNG)

**Таблица employees**
*id: INTEGER (Primary Key, Autoincrement)* - уникальный идентификатор сотрудника
*fullname: varchar(255)* - полное имя сотрудника
*specialization_id: INTEGER* - идентификатор специализации, связан с таблицей **specialization**
*salary: INTEGER* - зарплата сотрудника
![Пример записей из таблицы **employees**:](img/employees.PNG)

**Таблица record**
*id: INTEGER (Primary Key, Autoincrement)* - уникальный идентификатор записи
*client_id: INTEGER* - идентификатор клиента, связан с таблицей **clients**
*date: date* - дата записи
*service_id: INTEGER* - идентификатор услуги, связан с таблицей 
**services**
![Пример записей из таблицы **record** :](img/record.png)

**Таблица services**
*id: INTEGER (Primary Key, Autoincrement)* - уникальный идентификатор услуги
*box_id: INTEGER* - идентификатор ящика, связан с таблицей **boxes**
*service_cost: NUMERIC* - стоимость услуги
*name: VARCHAR(255)* - название услуги
![Пример записей из таблицы **services** :](img/services.PNG)

**Таблица service_station**
*id: INTEGER (Primary Key, Autoincrement)* - уникальный идентификатор станции обслуживания
*detail_id: INTEGER* - идентификатор детали, связан с таблицей **details**
*service_id: INTEGER* - идентификатор услуги, связан с таблицей **services**
![Пример записей из таблицы **service_station** :](img/service_station.PNG)

**Таблица specialization**
*id: INTEGER (Primary Key, Autoincrement)* - уникальный идентификатор специализации
*name: varchar(255)* - название специализации
![Пример записей из таблицы **specialization** :](img/specialization.PNG)