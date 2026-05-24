# cv

Online-резюме: **https://kudnever.github.io/cv/**

Single-page HTML + CSS, без сборщиков и зависимостей. Открывается в любом браузере локально (`open index.html`), деплоится через GitHub Pages.

## Структура

- `index.html` — содержание резюме
- `style.css` — оформление (включая dark mode + print-стили)

## Локально

```bash
# открыть в браузере
start index.html        # Windows
open index.html         # macOS
xdg-open index.html     # Linux
```

## PDF-экспорт

В браузере → Ctrl/Cmd + P → "Сохранить как PDF" → A4. Print-стили уже настроены под однотонную печать.

## Обновление

После пуша в `main` GitHub Pages автоматически передеплоит. Кэш браузера может держать старую версию пару минут — открыть в режиме инкогнито для проверки.
