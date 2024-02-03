Курсовой проект по БД
Программа получает данные о работодателях и их вакансиях с сайта hh.ru. Для этого используется публичный API hh.ru и библиотека requests.

Выбирает 10 компаний, от которых получает данные о вакансиях по API.

Полученные данные о работодателях и их вакансиях хранятся в таблицах в БД PostgreSQL. Для работы с БД используется библиотека psycopg2.

Реализован код, который заполняет созданные в БД PostgreSQL таблицы данными о работодателях и их вакансиях.
Создан класс DBManager для работы с данными в БД.
Класс DBManager подключается к БД PostgreSQL и имеет следующие методы:

get_companies_and_vacancies_count() — получает список всех компаний и количество вакансий у каждой компании.

get_all_vacancies() — получает список всех вакансий с указанием названия компании, названия вакансии и зарплаты и ссылки на вакансию.

get_avg_salary() — получает среднюю зарплату по вакансиям.

get_vacancies_with_higher_salary() — получает список всех вакансий, у которых зарплата выше средней по всем вакансиям.

get_vacancies_with_keyword() — получает список всех вакансий, в названии которых содержатся переданные в метод слова, например python.

Класс DBManager использует библиотеку psycopg2 для работы с БД.
