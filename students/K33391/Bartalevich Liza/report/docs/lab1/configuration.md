# Конфигурирование проекта

???+ question "Цель"

    Научится реализовывать полноценное серверное приложение с помощью фреймворка FastAPI с применением дополнительных средств и библиотек.

???+ question "Выбранная тема"

    Задача - создать веб-приложение, которое поможет людям находить партнеров для совместных путешествий. Приложение должно предоставлять возможность пользователям находить попутчиков для конкретных путешествий, обмениваться информацией о планируемых поездках и обсуждать детали маршрута. Функционал веб-приложения должен включать следующее:

    Создание профилей: Возможность пользователям создавать профили, указывать информацию о себе, своих навыках, опыте работы и предпочтениях по проектам.

    Создание поездок: Возможность пользователям создавать объявления о планируемых поездках с указанием дат, маршрута, предполагаемой длительности и других деталей.

    Поиск попутчиков: Функционал поиска попутчиков для конкретных поездок на основе заданных критериев, таких как место отправления, место назначения, даты и т.д.

    Управление поездками: Возможность управления созданными поездками, включая добавление/изменение деталей, отмену поездки и т.д.

Будем выполнять проект используя следующий набор python библиотек:

- fastapi
- uvicorn
- alembic
- sqlmodel

![Страница рейса](../assets/lab2/flight_1.png)

## Структура папок

```bash
├── alembic.ini
├── migrations
├── README.md
├── __init__.py
├── main.py
├── models.py
├── database.py
├── auth_manager.py
└── user_enpoints.py

```

- `models` - все модели нашего приложения. Не разношу по папкам, так как рекурсивные испорты в питоне это ад, а я уважаю свое время.
- `user_endpoints` - тут лежит настройка всех путей АПИ.
- `main` - тут лежит настройка всех путей для работы с юзером.
- `main` - выполняет роль сервисов и всего остального.

=== "main.py"

    ```Python title="Main"
    --8<-- "lab_1/main.py"
    ```