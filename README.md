| Команда           | Опис дії                                                                              |
| :---------------- | :------------------------------------------------------------------------------------ |
| `npm install`     | Встановлення всіх необхідних залежностей проєкту                                      |
| `npm run dev`     | Запуск локального сервера розробки Vite з гарячим оновленням (HMR)                    |
| `npm run build`   | Продакшн-збірка проєкту (компіляція Pug, SCSS, мінімізація у папку `dist`)            |
| `npm run preview` | Локальний попередній перегляд зібраної продакшн-версії з папки `dist`                 |
| `npm run format`  | Автоматичне форматування всіх файлів проєкту за допомогою Prettier                    |
| `npm run lint`    | Запуск повної перевірки стилів (Stylelint) та форматування (Prettier)                 |
| `npm run images`  | Генерація оптимізованих зображень у форматах `AVIF`, `WebP` та `JPG` (`400w`, `800w`) |

## Декомпозиція сторінки на BEM-блоки

**Layout (`l-`):** `l-container`, `l-grid` (`--debug`).
**State:** `is-visually-hidden`, далі `is-open` / `has-…` за потреби.

| Блок            | Елементи                                                                            | Модифікатори                    | Примітка                                       |
| --------------- | ----------------------------------------------------------------------------------- | ------------------------------- | ---------------------------------------------- |
| `skip-link`     | —                                                                                   | —                               | перехід до `main`                              |
| `header`        | `__logo`, `__actions`, `__action`                                                   | —                               | абсолютно поверх hero                          |
| `logo`          | `__img`                                                                             | —                               |                                                |
| `icon-button`   | `__icon`, `__text`                                                                  | `--phone`, `--menu`, `--close`  | hover телефону показує номер                   |
| `burger`        | `__line`                                                                            | `--top`, `--middle`, `--bottom` | довжини ліній змінюються на hover              |
| `menu`          | `__toggle`, `__panel`, `__header`, `__list`, `__item`, `__link`, `__phone`, `__cta` | —                               | checkbox + `:checked ~`, без JS                |
| `hero`          | `__media`, `__title`                                                                | —                               | `<picture>`, `fetchpriority="high"`            |
| `media`         | `__img`                                                                             | `--cover`, `--soft`             | кадрування, фон `#F9F9F9`, радіус 4            |
| `section-title` | —                                                                                   | —                               | заголовок будь-якої секції                     |
| `recommended`   | `__title`, `__list`, `__item`                                                       | —                               | `__item` = мікс з `product-card`               |
| `product-card`  | `__media`, `__name`, `__text`, `__price`                                            | —                               |                                                |
| `categories`    | `__title`, `__list`, `__item`, `__more`                                             | —                               | 6+6 / 3+3 / 1+1 колонок                        |
| `category`      | `__media`, `__label`                                                                | —                               |                                                |
| `button`        | —                                                                                   | —                               | default / hover / `:active` / `:focus-visible` |
| `timeless`      | `__banner`, `__body`, `__title`, `__text`                                           | —                               | кремовий фон `#FCFAEF`                         |
| `contacts`      | `__title`, `__form`, `__info`                                                       | —                               |                                                |
| `form`          | `__field`, `__submit`                                                               | —                               | `__submit` = мікс з `button`                   |
| `field`         | `__label`, `__control`                                                              | `--textarea`                    |                                                |
| `contact-info`  | `__item`, `__label`, `__value`                                                      | —                               | `tel:` / `mailto:`                             |
