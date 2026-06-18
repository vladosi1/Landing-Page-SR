# Landing Page · Система Розвитку

Статичний лендинг преміум-курсу Світлани Ретьман. Поки без збірника: тільки HTML, CSS і vanilla JS.

## Структура

- `index.html` — основна сторінка лендингу.
- `assets/css/style.css` — усі стилі лендингу.
- `assets/js/main.js` — інтерактив: програма, FAQ, відгуки, лічильники, reveal-анімації, модалка заявки.
- `assets/img/` — локальні зображення та логотипи.
- `preview-offline.html` — старий самодостатній preview-файл для перегляду без ассетів. Не використовувати як джерело для розробки.

## Інтеграція

1. HTML-секції з `index.html` можна переносити в окремий WordPress-шаблон або ACF-блоки.
2. CSS підключати окремим файлом через `wp_enqueue_style`.
3. JS підключати окремим файлом через `wp_enqueue_script` з `defer`.
4. Форма заявки зараз диспатчить подію `landingLeadSubmit`. До неї можна підключити Contact Form 7, WPForms або власний API.

## Ассети

Шляхи в коді відносні: `assets/img/...`, `assets/css/style.css`, `assets/js/main.js`. При переносі в тему WordPress замінити їх на `get_template_directory_uri()` або enqueue-логіку проекта.
