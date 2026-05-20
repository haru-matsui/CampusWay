# CampusWay

**CampusWay** — веб-портал и Telegram-бот для навигации по кампусу и жизни студентов.  
Проект помогает быстро находить аудитории, смотреть карту корпусов, узнавать о событиях и получать ответы на частые вопросы.

## Возможности

### Веб-портал
- быстрый поиск аудитории по номеру, описанию или корпусу;
- интерактивная карта кампуса по корпусам и этажам;
- список ближайших событий;
- подборка клубов и кружков;
- FAQ с ответами на популярные вопросы.

### Telegram-бот
- поддержка: передача сообщений администратору и ответ пользователю;
- мини-игра «Счастливый билет» — угадай преподавателя по предмету и группе.

## Технологии
- **Python** + **Flask** (веб-приложение)
- **Jinja2** (шаблоны)
- **aiogram** (Telegram-бот)
- HTML/CSS/JS + JSON-данные

## Структура проекта

```
README.md
hakaton1/
  Презентация.pptx
  hacaton/
    app.py                 # Flask-приложение
    bot.py                 # Telegram-бот
    teachers.json          # данные для игры бота
    templates/             # HTML-шаблоны страниц
    static/
      style.css
      data/                # JSON-данные (события, FAQ, клубы, аудитории)
      maps/                # изображения карт корпусов/этажей
      images/              # изображения для карточек и страниц
```

## Быстрый старт

### 1) Веб-приложение

```bash
cd hakaton1/hacaton
python -m venv .venv
source .venv/bin/activate      # Windows: .venv\Scripts\activate
pip install flask
python app.py
```

Откройте в браузере: `http://127.0.0.1:5000`.

### 2) Telegram-бот

```bash
cd hakaton1/hacaton
python -m venv .venv
source .venv/bin/activate      # Windows: .venv\Scripts\activate
pip install aiogram
python bot.py
```

Перед запуском укажите свой **TOKEN** и **ADMIN_ID** в `bot.py`.  
Не храните токен в открытом виде и не коммитите его в репозиторий.

## Данные

- `static/data/auditoriums.json` — аудитории для поиска
- `static/data/events.json` — события
- `static/data/clubs.json` — клубы
- `static/data/faq.json` — вопросы и ответы
- `teachers.json` — преподаватели для игры бота

## Материалы

В папке `hakaton1/` лежат презентация и дополнительные материалы проекта.
