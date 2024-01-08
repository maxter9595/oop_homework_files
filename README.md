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
```python
my_CookBook2 = GetCookBook(['recipes.txt'], ['Запеченный картофель', 'Омлет', 'Утка по-пекински']).get_cook_book_dict()
print(my_CookBook2)
```

## Задача № 2. Построение функции get_shop_list_by_dishes
Текст


