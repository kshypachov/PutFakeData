# Скрипт для відправки фейкових даних

Цей репозиторій містить скрипт Python, який використовує бібліотеку `Faker` для генерації фейкових даних користувача та надсилає ці дані на сервер через POST-запити.

## Встановлення

Щоб скролувати репозиторій,виконайте наступні команди

```bash
   git clone https://github.com/kshypachov/PutFakeData.git
   cd PutFakeData
   ```

Щоб встановити необхідні залежності, виконайте наступну команду:

```bash
pip3 install -r requirements.txt
```

## Використання

Скрипт генерує фейкові дані користувача, такі як ім'я, прізвище, по батькові, дата народження, РНОКПП, номер УНЗР, номер паспорта та стать, і надсилає ці дані на локальний сервер за адресою `http://127.0.0.1:8000/person`. Скрипт повторює цей процес 1000 разів.



## Опис змінних

- `fake`: Об'єкт класу `Faker`, налаштований для використання української локалі.
- `url`: URL-адреса, на яку будуть надсилатися дані.
- `count`: Кількість запитів, які будуть виконані.

## Перевірка JSON

Перед відправкою даних, JSON-об'єкт перевіряється на валідність за допомогою спроби завантаження його з рядка.

## Запит POST

Запит виконується з використанням бібліотеки `requests`. Заголовок вказує, що дані надсилаються у форматі JSON. Успішні запити відображають відповідь сервера, а помилкові — статусний код і текст відповіді.

## Ліцензія

Цей проект ліцензовано на умовах MIT License - див. файл LICENSE для подробиць.