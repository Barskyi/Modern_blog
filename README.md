# Django Blog App

## Огляд проекту

Цей проект представляє собою повнофункціональний блоговий додаток, розроблений на Django. Додаток дозволяє публікувати дописи, додавати теги, коментувати, ділитися дописами електронною поштою та шукати контент.

## Функціональність

### Основні можливості

- **Публікація дописів**: Система керування дописами з можливістю публікації, чернеток та різними статусами.
- **Теги**: Підтримка тегів для категоризації дописів з використанням бібліотеки `taggit`.
- **Коментарі**: Можливість додавати коментарі до дописів.
- **Пагінація**: Зручна навігація по списку дописів з пагінацією.
- **Рекомендаційна система**: Функціонал для відображення схожих дописів на основі спільних тегів.
- **Функція поділитися**: Можливість поділитися дописом по електронній пошті.
- **Пошук**: Повнотекстовий пошук по заголовкам та вмісту дописів з використанням PostgreSQL.

## Технічні деталі

### Використані технології

- **Django**: Основний фреймворк для розробки.
- **PostgreSQL**: База даних з підтримкою повнотекстового пошуку.
- **Django-taggit**: Бібліотека для реалізації системи тегів.

### Структура представлень (views)

- `post_list`: Відображення списку дописів з фільтрацією по тегам та пагінацією.
- `post_detail`: Детальне відображення посту з коментарями та схожими дописами.
- `post_share`: Функціонал для поділитися дописом через електронну пошту.
- `post_comment`: Обробка додавання коментарів до дописів.
- `post_search`: Повнотекстовий пошук по дописам з ранжуванням результатів.

## Встановлення

1. Клонуйте репозиторій
2. Створіть віртуальне середовище: `python -m venv venv`
3. Активуйте віртуальне середовище:
   - Windows: `venv\Scripts\activate`
   - Linux/Mac: `source venv/bin/activate`
4. Встановіть залежності: `pip install -r requirements.txt`
5. Налаштуйте базу даних PostgreSQL
6. Застосуйте міграції: `python manage.py migrate`
7. Запустіть сервер: `python manage.py runserver`

## Налаштування

Для правильної роботи додатку потрібно налаштувати:

1. Підключення до PostgreSQL в `settings.py`
2. Налаштування електронної пошти для функції "поділитися"
3. Опціональні налаштування для кількості дописів на сторінці (за замовчуванням 3)

## Використання

- Доступ до адмін-панелі: `/admin/`
- Список дописів: `/`
- Перегляд допису: `/рік/місяць/день/slug-допису/`
- Пошук: `/search/`

## Розробник

Barskyi Taras

