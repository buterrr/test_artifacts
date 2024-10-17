#### Задание: 7

Найдите номера моделей и цены всех имеющихся в продаже продуктов (любого типа) производителя B (латинская буква). 

#### Запрос:
```
SELECT a.model, a.price
FROM (SELECT model, price FROM PC
UNION
SELECT model, price FROM Laptop
UNION
SELECT model, price FROM Printer) AS a
JOIN Product
ON a.model = Product.model
WHERE maker = 'B'
```
___
#### Краткая информация о базе данных "Компьютерная фирма":

![computers](https://github.com/user-attachments/assets/e3e2bc5d-ea98-466e-b220-00c57830618d)

**Схема БД состоит из четырех таблиц:**

* Product(maker, model, type)

* PC(code, model, speed, ram, hd, cd, price)

* Laptop(code, model, speed, ram, hd, price, screen)

* Printer(code, model, color, type, price)

Таблица Product представляет производителя (maker), номер модели (model) и тип ('PC' - ПК, 'Laptop' - ПК-блокнот или 'Printer' - принтер).
Предполагается, что номера моделей в таблице Product уникальны для всех производителей и типов продуктов. В таблице PC для каждого ПК, 
однозначно определяемого уникальным кодом – code, указаны модель – model (внешний ключ к таблице Product), скорость - speed (процессора в мегагерцах), 
объем памяти - ram (в мегабайтах), размер диска - hd (в гигабайтах), скорость считывающего устройства - cd (например, '4x') и цена - price (в долларах). 
Таблица Laptop аналогична таблице РС за исключением того, что вместо скорости CD содержит размер экрана -screen (в дюймах). В таблице Printer для каждой модели принтера указывается, 
является ли он цветным - color ('y', если цветной), тип принтера - type (лазерный – 'Laser', струйный – 'Jet' или матричный – 'Matrix') и цена - price.
