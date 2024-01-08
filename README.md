# Домашнее задание к лекции «Открытие и чтение файла, запись в файл»

Решение [домашнего задания](https://github.com/netology-code/py-homeworks-basic/tree/master/7.files) приведено в файле Files.py. Текстовые файлы, задействованные для выведения кода, приведены в текущем репозитории.

## Задача № 1. Создание словаря cook_book
Словарь cook_book создан. Для его формирования были задействованы классы OpenFiles (чтение текстового файла) и GetCookBook (выведение словаря cook_book). Результат работы - возможность вызова словаря cook_book через метод get_cook_book_dict. Вызов метода был проведен следующим образом:

```GetCookBook``` ( ```file_name_list``` , ```our_product_list``` ).```get_cook_book_dict()```

```file_name_list``` - список наименований файлов TXT

```our_product_list``` - список блюд (по умолчанию заполняется полный перечень блюд из файла recipes.txt)

Примеры вызова метода get_cook_book_dict представлены ниже:

```python
my_CookBook1 = GetCookBook(['recipes.txt']).get_cook_book_dict()
print(my_CookBook1)
```
```
{'Омлет': [{'ingredient_name': 'Яйцо', 'quantity': 2, 'measure': 'шт'},
{'ingredient_name': 'Молоко', 'quantity': 100, 'measure': 'мл'},
{'ingredient_name': 'Помидор', 'quantity': 2, 'measure': 'шт'}],
'Утка по-пекински': [{'ingredient_name': 'Утка', 'quantity': 1, 'measure': 'шт'},
{'ingredient_name': 'Вода', 'quantity': 2, 'measure': 'л'},
{'ingredient_name': 'Мед', 'quantity': 3, 'measure': 'ст.л'},
{'ingredient_name': 'Соевый соус', 'quantity': 60, 'measure': 'мл'}],
'Запеченный картофель': [{'ingredient_name': 'Картофель', 'quantity': 1, 'measure': 'кг'},
{'ingredient_name': 'Чеснок', 'quantity': 3, 'measure': 'зубч'},
{'ingredient_name': 'Сыр гауда', 'quantity': 100, 'measure': 'г'}],
'Фахитос': [{'ingredient_name': 'Говядина', 'quantity': 500, 'measure': 'г'},
{'ingredient_name': 'Перец сладкий', 'quantity': 1, 'measure': 'шт'},
{'ingredient_name': 'Лаваш', 'quantity': 2, 'measure': 'шт'},
{'ingredient_name': 'Винный уксус', 'quantity': 1, 'measure': 'ст.л'},
{'ingredient_name': 'Помидор', 'quantity': 2, 'measure': 'шт'}]}
```
```python
my_CookBook2 = GetCookBook(['recipes.txt'], ['Запеченный картофель', 'Омлет', 'Утка по-пекински']).get_cook_book_dict()
print(my_CookBook2)
```
```
{'Запеченный картофель': [{'ingredient_name': 'Картофель', 'quantity': 1, 'measure': 'кг'},
{'ingredient_name': 'Чеснок', 'quantity': 3, 'measure': 'зубч'},
{'ingredient_name': 'Сыр гауда', 'quantity': 100, 'measure': 'г'}],
'Омлет': [{'ingredient_name': 'Яйцо', 'quantity': 2, 'measure': 'шт'},
{'ingredient_name': 'Молоко', 'quantity': 100, 'measure': 'мл'},
{'ingredient_name': 'Помидор', 'quantity': 2, 'measure': 'шт'}],
'Утка по-пекински': [{'ingredient_name': 'Утка', 'quantity': 1, 'measure': 'шт'},
{'ingredient_name': 'Вода', 'quantity': 2, 'measure': 'л'},
{'ingredient_name': 'Мед', 'quantity': 3, 'measure': 'ст.л'},
{'ingredient_name': 'Соевый соус', 'quantity': 60, 'measure': 'мл'}]}
```

## Задача № 2. Построение функции get_shop_list_by_dishes
Функция get_shop_list_by_dishes построена. Данная функция предполагает задействование функционала классов OpenFiles (чтение текстового файла), GetCookBook (выведение словаря cook_book) и GetShopList (выведение списка ингридиентов на основе словаря cook_book). Результат работы - возможность вызова функции get_shop_list_by_dishes.

```get_shop_list_by_dishes``` ( ```dishes``` , ```person_count``` )

```dishes``` - список блюд из словаря cook_book (по умолчанию заполняются все блюда, указанные в словаре cook_book)

```person_count``` - список блюд (по умолчанию заполняется одна персона)

Примеры использования функции get_shop_list_by_dishes представлены ниже:
```python
get_shop_list_by_dishes(['Запеченный картофель', 'Омлет'], 2)
```
```
{'Картофель': {'measure': 'кг', 'quantity': 2},
'Молоко': {'measure': 'мл', 'quantity': 200},
'Помидор': {'measure': 'шт', 'quantity': 4},
'Сыр гауда': {'measure': 'г', 'quantity': 200},
'Чеснок': {'measure': 'зубч', 'quantity': 6},
'Яйцо': {'measure': 'шт', 'quantity': 4}}
```
```python
get_shop_list_by_dishes(['Запеченный картофель', 'Омлет'])
```
```
{'Картофель': {'measure': 'кг', 'quantity': 1},
'Молоко': {'measure': 'мл', 'quantity': 100},
'Помидор': {'measure': 'шт', 'quantity': 2},
'Сыр гауда': {'measure': 'г', 'quantity': 100},
'Чеснок': {'measure': 'зубч', 'quantity': 3},
'Яйцо': {'measure': 'шт', 'quantity': 2}}
```
```python
get_shop_list_by_dishes()
```
```
{'Винный уксус': {'measure': 'ст.л', 'quantity': 1},
'Вода': {'measure': 'л', 'quantity': 2},
'Говядина': {'measure': 'г', 'quantity': 500},
'Картофель': {'measure': 'кг', 'quantity': 1},
'Лаваш': {'measure': 'шт', 'quantity': 2},
'Мед': {'measure': 'ст.л', 'quantity': 3},
'Молоко': {'measure': 'мл', 'quantity': 100},
'Перец сладкий': {'measure': 'шт', 'quantity': 1},
'Помидор': {'measure': 'шт', 'quantity': 4},
'Соевый соус': {'measure': 'мл', 'quantity': 60},
'Сыр гауда': {'measure': 'г', 'quantity': 100},
'Утка': {'measure': 'шт', 'quantity': 1},
'Чеснок': {'measure': 'зубч', 'quantity': 3},
'Яйцо': {'measure': 'шт', 'quantity': 2}}
```
```python
get_shop_list_by_dishes(person_count = 2)
```
```
{'Винный уксус': {'measure': 'ст.л', 'quantity': 2},
'Вода': {'measure': 'л', 'quantity': 4},
'Говядина': {'measure': 'г', 'quantity': 1000},
'Картофель': {'measure': 'кг', 'quantity': 2},
'Лаваш': {'measure': 'шт', 'quantity': 4},
'Мед': {'measure': 'ст.л', 'quantity': 6},
'Молоко': {'measure': 'мл', 'quantity': 200},
'Перец сладкий': {'measure': 'шт', 'quantity': 2},
'Помидор': {'measure': 'шт', 'quantity': 8},
'Соевый соус': {'measure': 'мл', 'quantity': 120},
'Сыр гауда': {'measure': 'г', 'quantity': 200},
'Утка': {'measure': 'шт', 'quantity': 2},
'Чеснок': {'measure': 'зубч', 'quantity': 6},
'Яйцо': {'measure': 'шт', 'quantity': 4}}
```

