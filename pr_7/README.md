# Отчет о выполнении практической работы №7. Выполнил студент группы ББМО-01-23 Бакин Д.И.

DVWA - это платформа для анализа угроз и уязвимостей

## Command Injection
Уязвимость позволяет с помощью веб-сервера выполнять произвольные команды в операционной системе хоста.
команда возможна, когда приложение передает небезопасные данные, предоставленные пользователем.

считываем содержимое файла

![ci1](https://github.com/xoz0r/Protected-Inform-Tech/assets/145142526/7493a5af-e4c0-4d86-b529-2607e8e8aff7)

![ci2](https://github.com/xoz0r/Protected-Inform-Tech/assets/145142526/cd676b93-c834-48dd-86c0-6e662b2163d5)

## File Inclusion
Уязвимость возможна, когда отсутствует корректная обработка входящих данных, и злоумышленник может манипулировать входящей информацией, инъектировать свои команды и включать другие файлы с веб-сервера.

видим вывод паролей

![fi1](https://github.com/xoz0r/Protected-Inform-Tech/assets/145142526/63ff4e0b-4899-476d-91df-61d56961d1e8)

## SQL Injection
Уязвимость, которая позволяет атакующему использовать фрагмент вредоносного кода на языке структурированных запросов (SQL) для манипулирования базой данных и получения доступа к потенциально ценной информации.

![SQL](https://github.com/xoz0r/Protected-Inform-Tech/assets/145142526/ffd10329-06fd-4230-b539-87c5e0b6269f)

## XSS reflected

межсайтовый скриптинг

Уязвимость дает возможность выполнения произвольного JavaScript-кода в браузере жертвы в контексте вашего сайта.

![xss](https://github.com/xoz0r/Protected-Inform-Tech/assets/145142526/ac0c459f-868d-46f0-b5c9-0321b482d2f2)

# Часть 2

Проверка работоспособности до добавления правил

![x2](https://github.com/xoz0r/Protected-Inform-Tech/assets/145142526/e510945c-1440-4985-a2cf-d60ea3c76583)

Добавление новых правил


![x3](https://github.com/xoz0r/Protected-Inform-Tech/assets/145142526/5d8eb767-8197-4073-a9a5-0fccd23f655f)

Далее перезапускаем контейнер для обновления правил WAF'a

Запуск exploration.py после приминения правил

![x4](https://github.com/xoz0r/Protected-Inform-Tech/assets/145142526/9fa5b72d-a998-4991-95f3-ecfbe8f91a62)

