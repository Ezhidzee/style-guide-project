# Restaurant Booking Documentation Style Guide

Учебный Docs as Code проект с правилами для документации микросервисного сервиса бронирования ресторанов. Руководство предназначено для разработчиков и технических писателей, которые описывают пользовательские сценарии, API, конфигурацию и эксплуатационные действия.

## Структура

- `docs/` — страницы стайлгайда и примеры документов.
- `mkdocs.yml` — навигация и параметры сайта.
- `.github/workflows/docs.yml` — проверки и публикация GitHub Pages.
- `CONTRIBUTING.md` — порядок внесения изменений.

## Установка и запуск

В PowerShell создайте виртуальное окружение и установите зависимости:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

Запустите локальный сайт:

```powershell
python -m mkdocs serve
```

## Проверки

Перед отправкой изменений выполните:

```powershell
npx --yes markdownlint-cli@0.45.0 "**/*.md" "#site"
python -m mkdocs build --strict
git diff --check
```

