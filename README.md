# Домашнее задание к лекции «Открытие и чтение файла, запись в файл»

Решение [домашнего задания](https://github.com/netology-code/py-homeworks-basic/tree/master/7.files) приведено в файле Files.py.

## Задача № 1. Создание словаря cook_book
Словарь cook_book создан. Для его формирования были задействованы классы OpenFiles (чтение текстового файла recipes.txt) и GetCookBook (выведение словаря cook_book). Результат работы - возможность вызова словаря cook_book через метод get_cook_book_dict. Структура вызова:

GetCookBook(```file_name_list``` , ```our_product_list```).get_cook_book_dict()

```file_name_list``` - список наименований файлов TXT (при необходимости указывается путь к файлам)

```our_product_list``` - список блюд (по умолчанию заполняется полный перечень блюд, содержащийся в файле recipes.txt)

Проверка работоспособности вызова словаря cook_book представлена в следующей части кода:

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
print('Словарь cook_book (роверка на ошибки - пустой список):')
print(GetCookBook(['recipes.txt'], []).get_cook_book_dict())
print()
```
