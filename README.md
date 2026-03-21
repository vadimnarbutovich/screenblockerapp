# ScreenBlocker — сайт для GitHub Pages

Статический лендинг и страницы политики конфиденциальности в визуальном стиле приложения (неон, «стекло», тёмный градиентный фон).

## Что внутри

| Файл | Назначение |
|------|------------|
| `index.html` | Главная: фичи, плейсхолдеры скриншотов, ссылки на политики |
| `privacy-en.html` | Privacy Policy (English, достаточно для типичного App Store review) |
| `styles.css` | Общие стили |
| `.nojekyll` | Отключает Jekyll на GitHub Pages (важно для файлов с `_` в имени и предсказуемой раздачи статики) |
| `assets/` | Иконка и скриншоты (см. `assets/README.md`) |

## Публикация в репозиторий `screenblockerapp`

Репозиторий на GitHub: [vadimnarbutovich/screenblockerapp](https://github.com/vadimnarbutovich/screenblockerapp).

1. Клонируйте пустой репозиторий (или инициализируйте git в пустой папке и добавьте `origin`).
2. **Скопируйте содержимое этой папки** (`Website/screenblockerapp/` из монорепо ScreenBlocker) **в корень** клона — чтобы в корне лежали `index.html`, `styles.css`, `.nojekyll` и т.д.
3. Добавьте в `assets/` файлы `appicon.png`, `screen-0.png` … и раскомментируйте соответствующие теги в `index.html` (см. подсказки в HTML).
4. В `index.html` замените ссылку кнопки «Download» на реальный URL в App Store.
5. Коммит и push в ветку `main` (или `master`).

### Включить GitHub Pages

В репозитории: **Settings → Pages → Build and deployment → Source**: **Deploy from a branch** → Branch **`main`** (или ваша основная ветка), папка **`/ (root)`** → Save.

Сайт будет доступен по адресу вида `https://vadimnarbutovich.github.io/screenblockerapp/` (точный URL покажет GitHub после деплоя).

## Локальный просмотр

Откройте `index.html` в браузере или поднимите простой сервер:

```bash
python3 -m http.server 8080
```

Затем `http://localhost:8080`.
