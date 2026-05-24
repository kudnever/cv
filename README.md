# cv

Резюме Ильи Малкина в трёх форматах.

## Онлайн-версия

**https://kudnever.github.io/cv/** (на русском, с фото и dark mode)

## PDF

- `kudnever-cv-en.pdf` · английская версия для EU / LinkedIn / прямого аутрича
- `kudnever-cv-ru.pdf` · русская версия для hh.ru / RU-аутрича

Обе сгенерированы из соответствующих HTML через headless Edge.

## Структура

| Файл | Назначение |
|---|---|
| `index.html` + `style.css` + `photo.jpg` | онлайн-версия (GitHub Pages) |
| `cv-en-pdf.html` | source для англоязычного PDF |
| `cv-ru-pdf.html` | source для русскоязычного PDF |
| `kudnever-cv-en.pdf` | готовый английский PDF |
| `kudnever-cv-ru.pdf` | готовый русский PDF |

## Локальная пересборка PDF

```powershell
$edge = "C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe"
$profile = "C:\Users\V\AppData\Local\Temp\edge-cv"

# EN
& $edge --headless --disable-gpu --no-pdf-header-footer --print-to-pdf-no-header `
  --user-data-dir=$profile `
  --print-to-pdf="kudnever-cv-en.pdf" "file:///$(Resolve-Path cv-en-pdf.html)"

# RU
& $edge --headless --disable-gpu --no-pdf-header-footer --print-to-pdf-no-header `
  --user-data-dir=$profile `
  --print-to-pdf="kudnever-cv-ru.pdf" "file:///$(Resolve-Path cv-ru-pdf.html)"
```

## Обновление онлайн-версии

После пуша в `main` GitHub Pages автоматически передеплоит. Кэш браузера может держать старую версию пару минут, поэтому при проверке открой в режиме инкогнито.
