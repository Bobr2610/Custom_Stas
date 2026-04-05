# Custom Overlay Counter

## Пример с моими статами

[![Stats](https://raw.githubusercontent.com/Bobr2610/Custom_Stas/ae0227e59a5877301cf49e86a15541c5d29babbe/counter.png)](https://github.com/Bobr2610/Custom_Stas)

Отображает **Total Contributions**, **Current Streak** и **Longest Streak** поверх вашего фонового изображения.

---

## Настройка

### 1. Настройте фоновое изображение

Положите ваше изображение в папку `Theme/` (или `theme/`). Для темы с бобрами (`theme_beavers.png`) workflow автоматически разместит **Total Contributions**, **Current Streak** и **Longest Streak** поверх изображения.

### 2. (Опционально) Свои цифры

Положите изображения цифр в папку `Theme/` (или `theme/`) с именами `0.png`, `1.png`, ... `9.png`. Если их нет, будут созданы автоматически.

### 3. Запуск

- **Автоматически:** каждый час и при пуше
- **Вручную:** **Actions** → **Update Overlay Counter** → **Run workflow**

Пользователь определяется автоматически по владельцу репозитория (`github.repository_owner`).

---

## Структура файлов

```
├── .github/workflows/update-counter.yml
├── Theme/
│   ├── theme_beavers.png  (тема с бобрами — 3 области для статистики)
│   ├── 0.png ... 9.png   (цифры, создаются автоматически)
│   └── *.png             (другие фоновые изображения)
├── counter.json          (fallback при сбое API: {"total": N, "current": N, "longest": N})
├── counter.png           (генерируется)
└── README.md
```
