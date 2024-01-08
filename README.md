# Домашнее задание к лекции «Открытие и чтение файла, запись в файл»

Решение [домашнего задания](https://github.com/netology-code/py-homeworks-basic/tree/master/7.files) приведено в файле Files.py. Текстовые файлы, задействованные для выведения кода, приведены в текущем репозитории.

## Задача № 1. Создание словаря cook_book
Словарь _**cook_book**_ создан. Для его формирования были задействованы классы _**OpenFiles**_ (чтение текстового файла recipes.txt) и _**GetCookBook**_ (выведение словаря cook_book). Результат работы - возможность вызова словаря _**cook_book**_ через метод _**get_cook_book_dict**_. Вызов метода был проведен следующим образом:

**`GetCookBook`**( ```file_name_list``` , ```our_product_list``` ).**`get_cook_book_dict()`**

```file_name_list``` - список наименований файлов TXT

```our_product_list``` - список блюд (по умолчанию заполняется полный перечень блюд из файла recipes.txt)

Проверка работоспособности вызова метода get_cook_book_dict представлена в следующей части кода:

```python
print('***** Результат получения словаря cook_book *****')
print()
print('Словарь cook_book (полная версия):')
print(GetCookBook(['recipes.txt']).get_cook_book_dict())
print()
print('Словарь cook_book (выборочная версия):')
print(GetCookBook(['recipes.txt'], ['Запеченный картофель', 'Омлет', 'Утка по-пекински']).get_cook_book_dict())
print()
print('Словарь cook_book (проверка на ошибки - ввод отсутствующих блюд):')
print(GetCookBook(['recipes.txt'], ['Биг мак', 'Роял чизбургер', 'Картошка фри', 'Фахитос']).get_cook_book_dict())
print()
print('Словарь cook_book (проверка на ошибки - отсутствие списка блюд):')
print(GetCookBook(['recipes.txt'], 'Hello world!').get_cook_book_dict())
print()
print('Словарь cook_book (проверка на ошибки - пустой список):')
print(GetCookBook(['recipes.txt'], []).get_cook_book_dict())
print()
```
