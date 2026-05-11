# myresume

Личный сайт. Деплоится на GitHub Pages через GitHub Actions при пуше в `main`.

## Структура

- `index.html` — единственная страница сайта (адаптивная, без библиотек)
- `resume/` — резюме: `ivan_ilin_developer.tex` (исходник) и `ivan_ilin_developer.pdf`. CI пересобирает PDF из `.tex` перед деплоем.
- `.github/workflows/deploy.yml` — пайплайн деплоя

## Локально

Открыть `index.html` в браузере, либо:

```sh
python3 -m http.server 8000
```

## Деплой

1. Создай репозиторий на GitHub и запушь `main`.
2. В настройках репо: **Settings → Pages → Source = GitHub Actions**.
3. Каждый пуш в `main` запускает workflow и публикует сайт.

## Обновление резюме

Редактируй `resume/ivan_ilin_developer.tex` — CI пересоберёт PDF при пуше. Локально можно собрать через `cd resume && ./build.sh` (Docker) или `pdflatex ivan_ilin_developer.tex`.
