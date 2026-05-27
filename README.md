# cv

Резюме Ильи Малкина в двух языках.

## Готовые PDF

- [`kudnever-cv-en.pdf`](kudnever-cv-en.pdf) · английская версия (EU / LinkedIn / прямой аутрич)
- [`kudnever-cv-ru.pdf`](kudnever-cv-ru.pdf) · русская версия (hh.ru / RU-аутрич)

Прямые ссылки для отправки рекрутерам:
- https://github.com/kudnever/cv/raw/main/kudnever-cv-en.pdf
- https://github.com/kudnever/cv/raw/main/kudnever-cv-ru.pdf

## Source

- `cv-en-pdf.html` · source англоязычного PDF
- `cv-ru-pdf.html` · source русскоязычного PDF

A4, single-column, ATS-friendly, без em-dashes. Стиль зеркалит классический backend-CV: SUMMARY, PROJECTS, TECHNICAL SKILLS, EDUCATION, LANGUAGES.

## Пересборка PDF

PowerShell:

```powershell
$edge = "C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe"
$profile = "$env:TEMP\edge-cv"

& $edge --headless --disable-gpu --no-pdf-header-footer --print-to-pdf-no-header `
  --user-data-dir=$profile `
  --print-to-pdf="kudnever-cv-en.pdf" "file:///$(Resolve-Path cv-en-pdf.html)"

& $edge --headless --disable-gpu --no-pdf-header-footer --print-to-pdf-no-header `
  --user-data-dir=$profile `
  --print-to-pdf="kudnever-cv-ru.pdf" "file:///$(Resolve-Path cv-ru-pdf.html)"
```
