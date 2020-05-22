<h1 align="center">
<br>
  <img src="https://raw.githubusercontent.com/thedaviddias/Front-End-Checklist/master/data/images/logo-front-end-checklist.jpg" alt="Front-End Checklist" width="170">
  <br>
    <br>
  Front-End Checklist
  <br>
</h1>

<h4 align="center">The Front-End Checklist это исчерпывающий список элементов сайта или HTML страницы, которые должны быть проверены перед выпуском в production</h4>

<p align="center">
   <a href=“http://makeapullrequest.com">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square" alt="PRs Welcome">
    </a>
    <a href=“https://github.com/thedaviddias/Front-End-Checklist/graphs/contributors">
    <img src="https://img.shields.io/github/contributors/thedaviddias/Front-End-Checklist.svg?style=flat-square" alt="Contributors">
  </a>
  <a href=“https://gitter.im/Front-End-Checklist/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link">
    <img src="https://img.shields.io/badge/chat-on_gitter-008080.svg?style=flat-square" alt="Gitter">
  </a>
      <a href=“https://github.com/thedaviddias/Front-End-Checklist/">
    <img src="https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg?style=flat-square" alt="Front‑End_Checklist followed">
</a>
    <a href=“https://creativecommons.org/publicdomain/zero/1.0/">
    <img src="https://img.shields.io/badge/license-CC0-green.svg?style=flat-square" alt="CC0">
  </a>
</p>

<p align="center">
  <a href="#Как-этим-пользоваться">Как пользоваться</a> •
  <a href="#contributing">Contributing</a> •
  <a href="https://frontendchecklist.io">Сайт</a>
  <a href="https://www.producthunt.com/posts/front-end-checklist">Product Hunt</a>
</p>
<p align="center">
    <span>Другие чек-дисты:</span>
    <br>
  <a href="https://github.com/thedaviddias/Front-End-Performance-Checklist#---------front-end-performance-checklist-">🎮 Front-End Performance Checklist</a> • <a href="https://github.com/thedaviddias/Front-End-Design-Checklist#front-end-design-checklist">💎 Front-End Design Checklist</a>
</p>

Он основан на многолетнем опыте front-end разработчиков и, кроме того, включает в себя части других открытых checklist-ов.

## Содержание

1. **[Head](#head)**
2. **[HTML](#html)**
3. **[Web-шрифты](#web-шрифты)**
4. **[CSS](#css)**
5. **[Картинки](#Картинки)**
6. **[JavaScript](#javascript)**
7. **[Безопасность](#Безопасность)**
8. **[Производительность](#Производительность)**
9. **[Доступность](#Доступность)**
10. **[SEO](#seo)**

## Как этим пользоваться?

Все пункты **Front-End Checklist** обязательны для большинства сайтов, однако некоторые элементы могут быть менее важны или вовсе пропущены (например если вам не нужен RSS для админки приложения). Мы выбрали 3 уровня гибкости:

- ![Low][low_img] означает, что пункт **рекомендован**, но может быть пропущен в некоторых случаях.
- ![Medium][medium_img] элемент **крайне рекомендован** и может быть пропущен только в очень специфических ситуациях. Невыполнение некоторых пунктов может иметь негативные последствия, например с точки производительности или SEO.
- ![High][high_img] такой пункт **обязателен**. Может сломать страницу или привести к проблемам с доступностью (accessibility) и SEO. Проверяйте такие элементы в первую очередь.

Некоторые комментарии снабжены иконками, чтобы вы лучше понимали, какой контент или помощь можно найти:

- 📖: документация или статья
- 🛠: он-лайн инструменты / утилиты для проверки
- 📹: медиа или видео контент

> Если хотите внести вклад в **_Front-End Checklist App_**, прочтите [README_APP file](https://github.com/thedaviddias/Front-End-Checklist/blob/master/README_APP.md).

---

## Head

> **Примечание:** Можно посмотреть [список всего](https://github.com/joshbuchea/HEAD), что может быть в `<head>` HTML документа.

### Мета-теги

- [ ] **Doctype:** ![High][high_img] Doctype относится к HTML5 и находится в самом верху HTML страниц.

```html
<!DOCTYPE html>
<!-- HTML5 -->
```

> - 📖 [Определение кодировки (англ.) - HTML5 W3C](https://www.w3.org/TR/html5/syntax.html#determining-the-character-encoding)

_Следующие 2 мета-тега (Charset и Viewport) должны быть расположены в самом начале `<head>`._

- [ ] **Charset:** ![High][high_img] Кодировка (UTF-8) задана правильно.

```html
<!-- Задать кодировку документа -->
<meta charset="utf-8" />
```

- [ ] **Viewport:** ![High][high_img] Viewport задан правильно.

```html
<!-- Задать viewport для responsive дизайна -->
<meta
  name="viewport"
  content="width=device-width, initial-scale=1, viewport-fit=cover"
/>
```

- [ ] **Title:** ![High][high_img] Задан на всех страницах (SEO: Google рассчитывает ширину символов в title и обрезает примерно от 472 до 482 пикселей. Так что предел длины title около 55 символов).

```html
<!-- Document Title -->
<title>Название короче 55 символов</title>
```

> - 📖 [Title - HTML - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title)
> - 🛠 [SERP Snippet Generator](https://www.sistrix.com/serp-snippet-generator/)

- [ ] **Description:** ![High][high_img] Description задан, уникален и короче 150 символов.

```html
<!-- Meta Description -->
<meta name="description" content="Описание страницы короче 150 символов" />
```

> - 📖 [Meta Description - HTML - MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#Adding_an_author_and_description)

- [ ] **Favicons:** ![Medium][medium_img] Иконки отображаются корректно. Если у вас только один `favicon.ico`, положите его в корень сайта. Обычно вам не нужно ничего добавлять в разметку. Однако, хорошей практикой считается сделать ссылку как в примере ниже. На сегодняшний день **рекомендован PNG формат** вместо `.ico`(разрешение: 32x32px).

```html
<!-- Стандартный favicon -->
<link rel="icon" type="image/x-icon" href="https://example.com/favicon.ico" />
<!-- Рекомендованный формат favicon -->
<link rel="icon" type="image/png" href="https://example.com/favicon.png" />
```

> - 🛠 [Favicon Generator](https://www.favicon-generator.org/)
> - 🛠 [RealFaviconGenerator](https://realfavicongenerator.net/)
> - 📖 [Favicon шпаргалка](https://github.com/audreyr/favicon-cheat-sheet)
> - 📖 [Favicons, Touch Icons, Tile Icons, etc. Which Do You Need? - CSS Tricks](https://css-tricks.com/favicon-quiz/)
> - 📖 [PNG favicons - caniuse](https://caniuse.com/#feat=link-icon-png)

- [ ] **Apple Web App Meta:** ![Low][low_img] Заданы мета-теги для Apple

```html
<!-- Apple Touch Icon (не меньше, чем 200x200px) -->
<link rel="apple-touch-icon" href="/custom-icon.png" />

<!-- Развернуть веб-приложение на полный экран -->
<meta name="apple-mobile-web-app-capable" content="yes" />

<!-- Задаёт стиль для Status Bar (возможные значения смотри по ссылке Supported Meta Tags ниже) -->
<!-- Не имеет эффекта, если не выставлен предыдущий тег -->
<meta name="apple-mobile-web-app-status-bar-style" content="black" />
```

> - 📖 [Configuring Web Applications](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)
> - 📖 [Supported Meta Tags](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html)

- [ ] **Windows Tiles:** ![Low][low_img] Windows tiles заданы.

```html
<!-- Microsoft Tiles -->
<meta name="msapplication-config" content="browserconfig.xml" />
```

Минимальный требуемый `browserconfig.xml`:

```xml
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
   <msapplication>
     <tile>
        <square70x70logo src="small.png"/>
        <square150x150logo src="medium.png"/>
        <wide310x150logo src="wide.png"/>
        <square310x310logo src="large.png"/>
     </tile>
   </msapplication>
</browserconfig>
```

> - 📖 [Browser configuration schema reference](<https://msdn.microsoft.com/en-us/library/dn320426(v=vs.85).aspx>)

- [ ] **Canonical:** ![Medium][medium_img] Используйте `rel="canonical"` чтобы избежать дублированности контента.

```html
<!-- Помогает избежать проблем с дублированным контентом -->
<link
  rel="canonical"
  href="http://example.com/2017/09/a-new-article-to-red.html"
/>
```

> - 📖 [Use canonical URLs - Search Console Help - Google Support](https://support.google.com/webmasters/answer/139066?hl=en)
> - 📖 [5 common mistakes with rel=canonical - Google Webmaster Blog](https://webmasters.googleblog.com/2013/04/5-common-mistakes-with-relcanonical.html)

### HTML теги

- [ ] **Атрибут lang:** ![High][high_img] Атрибут `lang` задан в соответствии с языком страницы.

```html
<html lang="en"></html>
```

- [ ] **Атрибут direction:** ![Medium][medium_img] Направление текста задано в этом атрибуте тега `html`. Также этот атрибут может быть применён к другим тегам.

```html
<html dir="rtl"></html>
```

> - 📖 [dir - HTML - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/dir)

- [ ] **Альтернативный язык:** ![Low][low_img] Тег языка задан и соответствует языку страницы.

```html
<link rel="alternate" href="https://es.example.com/" hreflang="es" />
```

- [ ] **Условные комментарии:** ![Low][low_img] Условные комментарии заданы для IE, если требуется.

> - 📖 [About conditional comments (Internet Explorer) - MSDN - Microsoft](<https://msdn.microsoft.com/en-us/library/ms537512(v=vs.85).aspx>)

- [ ] **RSS feed:** ![Low][low_img] Если ваш проект является блогом или содержит страницы, убедитесь, что RSS настроен.

- [ ] **Критичные CSS стили заданы inline:** ![Medium][medium_img] Критичный CSS (critical CSS) - CSS, задающий стили контента видимого сразу же пока идёт процесс загрузки страницы ("above the fold content"). Минифицируйте такой CSS и вставьте внутри `<style></style>` перед загрузкой остальных стилей.

  > - 🛠 Инструмент для автоматизации: [Critical by Addy Osmani on GitHub](https://github.com/addyosmani/critical)

- [ ] **Порядок CSS:** ![High][high_img] Все CSS файлы должны загружаться перед любыми JavaScript файлами в `<head>`. (За исключением случаев, когда JS файлы загружаются асинхронно в верху страницы).

### Социальные сети

**_Facebook OG_** и **_Twitter Cards_** крайне рекомендованы для всех сайтов. Добавьте теги для других соц. сетей, если планируете отображаться в них корретно.

- [ ] **Facebook Open Graph:** ![Low][low_img] Все теги All Facebook Open Graph (OG) протестированы, ни один не пропущен и информация в них верна. Картинки должны быть хотя бы 600 x 315 пикселей. Рекомендуемое разрешение 1200 x 630 пикселей.

> **Примечание:** Используйте `og:image:width` и `og:image:height` чтобы указать разрешение картинок для паука (the crawler) для того, чтобы картинки могли быть отрендерены сразу же. Иначе потребуется асинхронная подгрузка и обработка.

```html
<meta property="og:type" content="website" />
<meta property="og:url" content="https://example.com/page.html" />
<meta property="og:title" content="Content Title" />
<meta property="og:image" content="https://example.com/image.jpg" />
<meta property="og:description" content="Description Here" />
<meta property="og:site_name" content="Site Name" />
<meta property="og:locale" content="en_US" />
<!-- Следующие теги не обязательны, но рекомендованы -->
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
```

> - 📖 [A Guide to Sharing for Webmasters](https://developers.facebook.com/docs/sharing/webmasters/)
> - 📖 [Best Practices - Sharing](https://developers.facebook.com/docs/sharing/best-practices/)
> - 🛠 Протестируйте страницу с [Facebook OG testing](https://developers.facebook.com/tools/debug/)

- [ ] **Twitter Card:** ![Low][low_img]

```html
<meta name="twitter:card" content="summary" />
<meta name="twitter:site" content="@site_account" />
<meta name="twitter:creator" content="@individual_account" />
<meta name="twitter:url" content="https://example.com/page.html" />
<meta name="twitter:title" content="Content Title" />
<meta
  name="twitter:description"
  content="Content description less than 200 characters"
/>
<meta name="twitter:image" content="https://example.com/image.jpg" />
```

> - 📖 [Getting started with cards — Twitter Developers](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/guides/getting-started)
> - 🛠 Проверьте страницу с [Twitter card validator](https://cards-dev.twitter.com/validator)

**[⬆ наверх](#Содержание)**

---

## HTML

### Лучшие практики

- [ ] **Семантические элементы HTML5:** ![High][high_img] Семантические элементы HTML5 используются должным образом (header, section, footer, main...).

> - 📖 [HTML Reference](http://htmlreference.io/)

- [ ] **Страницы ошибок:** ![High][high_img] Страницы ошибок 404 и 5xx существуют. Не забывайте, что в страницы ошибок 5xx должны быть включены их стили, чтобы обойтись без подгрузки с сервера.

- [ ] **Noopener:** ![Medium][medium_img] Ссылки на внешние ресурсы с `target="_blank"` должны иметь атрибут `rel="noopener"`, чтобы предотвратить фишинговые атаки типа tab nabbing. Если нужно поддерживать старые версии Firefox, используйте `rel="noopener noreferrer"`.

> - 📖 [About rel=noopener](https://mathiasbynens.github.io/rel-noopener/)

- [ ] **Удаление комментариев:** ![Low][low_img] Ненужный код должен быть удалён перед отправкой в production.

### Тестирование HTML

- [ ] **W3C совместимость:** ![High][high_img] Все страницы должны быть проверены W3C валидатором.

> - 🛠 [W3C validator](https://validator.w3.org/)

- [ ] **HTML Lint:** ![High][high_img] Инструменты, которые помогают анализировать проблемы в HTML.

> - 🛠 [Dirty markup](https://dirtymarkup.com/)

> - 🛠 [Sonar a linting tool for the web](https://sonarwhal.com/)

- [ ] **Проверка ссылок:** ![High][high_img] Нет сломанных ссылок, нет ошибок 404.

> - 🛠 [W3C Link Checker](https://validator.w3.org/checklink)

- [ ] **Проверка на Adblock:** ![Medium][medium_img] Сайт корректно отображается c включёнными вырезателями рекламы типа Adblock. Можете показать специальное сообщение с просьбой выключить подобные плагины.

**[⬆ наверх](#Содержание)**

---

## Web-шрифты

> **Примечание:** Использование web-шрифтов может вызвать мерцание или исчезновение текста (FOUT - Flash of Unstyled Text, FOIT - Flash of Invisible Text). Так что убедитесь, что задан резервный шрифт, либо используйте загрузчик шрифтов чтобы держать ситуацию под контролем.
>
> - 📖 [Google Technical considerations about webfonts](https://developers.google.com/fonts/docs/technical_considerations)

- [ ] **Форматы web-шрифтов:** ![High][high_img] WOFF, WOFF2 и TTF поддерживаются всеми браузерами.

> - 📖 [WOFF - Web Open Font Format - Caniuse](https://caniuse.com/#feat=woff).
> - 📖 [WOFF 2.0 - Web Open Font Format - Caniuse](https://caniuse.com/#feat=woff2).
> - 📖 [TTF/OTF - TrueType and OpenType font support](https://caniuse.com/#feat=ttf)
> - 📖 [Using @font-face - CSS-Tricks](https://css-tricks.com/snippets/css/using-font-face/)

- [ ] **Размер web-шрифтов:** ![High][high_img] Размер шрифтов суммарно не превышает 2 MB.

- [ ] **Загрузчик web-шрифтов:** ![Low][low_img] Контролируйте закачку шрифтов с помощью загрузчика.

> - 🛠 [Typekit Web Font Loader](https://github.com/typekit/webfontloader)

**[⬆ наверх](#Содержание)**

---

## CSS

> **Примечание:** Ознакомьтесь с [CSS guidelines](https://cssguidelin.es/) и [Sass Guidelines](https://sass-guidelin.es/), которых придерживаются большинство разработчиков. Если у вас есть сомнения насчёт CSS свойств, посетите [CSS Reference](http://cssreference.io/). Кроме того взгляните на короткий гайд [Code Guide](http://codeguide.co/).

- [ ] **Отзывчивый (responsive) веб-дизайн:** ![High][high_img] Дизайн должен быть отзывчивым.
- [ ] **CSS для печати:** ![Medium][medium_img] Стили для печати заданы и работают корректны.
- [ ] **Препроцессоры:** ![Low][low_img] Используйте CSS препроцессоры (например [Sass](http://sass-lang.com/), [Less](http://lesscss.org/), [Stylus](http://stylus-lang.com/)).
- [ ] **Уникальные ID:** ![High][high_img] Если используются Id, убедитесь, что они уникальны в пределах страницы.
- [ ] **Сброс (reset) CSS:** ![High][high_img] Используются актуальные версии инструментов для нормализации CSS (reset, normalize или reboot). _(Если используете CSS фреймворк типа Bootstrap или Foundation, Normalize уже в них включён.)_

> - 📖 [Reset.css](https://meyerweb.com/eric/tools/css/reset/)
> - 📖 [Normalize.css](https://necolas.github.io/normalize.css/)
> - 📖 [Reboot](https://getbootstrap.com/docs/4.0/content/reboot/)

- [ ] **JS префиксы:** ![Low][low_img] Все классы и id, используемые в JS файлах, начинаются с префикса **js-** и не участвуют в назначении стилей.

```html
<div id="js-slider" class="my-slider">
  <!-- Или -->
  <div id="id-used-by-cms" class="js-slider my-slider"></div>
</div>
```

- [ ] **Embedded или inline CSS:** ![High][high_img] Любой ценой избегайте внедрения CSS в `<style>` теги (embeding) или inline стилей. Применяйте такие подходы только в особых случаях, например background-image для слайдера или critical CSS (см. выше).
- [ ] **Вендорные префиксы:** ![High][high_img] CSS вендорные префиксы используются и генерируются в соответствии с поддерживаемыми браузерами.

> - 🛠 [Autoprefixer CSS online](https://autoprefixer.github.io/)

### Производительность CSS

- [ ] **Конкатенация:** ![High][high_img] CSS файлы сконкатенированы в один файл. _(Не для HTTP/2)_.
- [ ] **Минификация:** ![High][high_img] Все CSS файлы минифицированы.
- [ ] **Неблокирующий CSS:** ![Medium][medium_img] CSS файлы должны быть неблокирующими DOM, чтобы избежать потерь времени.

> - 📖 [loadCSS by filament group](https://github.com/filamentgroup/loadCSS)
> - 📖 [Example of preload CSS using loadCSS](https://gist.github.com/thedaviddias/c24763b82b9991e53928e66a0bafc9bf)

- [ ] **Неиспользуемый CSS:** ![Low][low_img] Удалите неиспользуемые стили.

> - 🛠 [UnCSS Online](https://uncss-online.com/)
> - 🛠 [PurifyCSS](https://github.com/purifycss/purifycss)
> - 🛠 [PurgeCSS](https://github.com/FullHuman/purgecss)
> - 🛠 [Chrome DevTools Coverage](https://developers.google.com/web/updates/2017/04/devtools-release-notes#coverage)

### Тестирование CSS

- [ ] **Stylelint:** ![High][high_img] В CSS или SCSS файлах нет ошибок.

> - 🛠 [stylelint, a CSS linter](https://stylelint.io/)
> - 📖 [Sass guidelines](https://sass-guidelin.es/)

- [ ] **Отзывчивый web-дизайн:** ![High][high_img] Все страницы были протестированы на следующих контрольных точках: 320px, 768px, 1024px (может быть больше а зависимости от проекта).

- [ ] **CSS валидатор:** ![Medium][medium_img] CSS был протестирован, ошибки исправлены.

> - 🛠 [CSS Validator](https://jigsaw.w3.org/css-validator/)

- [ ] **Desktop браузеры:** ![High][high_img] Все страницы были протестированы на всех поддерживаемых desktop браузерах (Safari, Firefox, Chrome, Internet Explorer, EDGE...).
- [ ] **Мобильные браузеры:** ![High][high_img] Все страницы были протестированы на всех поддерживаемых мобильных браузерах (Native browser, Chrome, Safari...).
- [ ] **ОС:** ![High][high_img] Все страницы были протестированы на всех поддерживаемых ОС (Windows, Android, iOS, Mac...).

* [ ] **Точное соответствие макету:** ![Low][low_img] В зависимости от проекта и качества макета, перед вами может стоять задача сделать разметку идеально соответствующей дизайну. Используйте специальные инструменты, чтобы проверить вашу реализацию на соответствие макету.

> [Pixel Perfect - Chrome Extension](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en)

- [ ] **Направление текста:** ![High][high_img] Все страницы должны быть протестированы в LTR и RTL языках, если они поддерживаются.

> - 📖 [Building RTL-Aware Web Apps & Websites: Part 1 - Mozilla Hacks](https://hacks.mozilla.org/2015/09/building-rtl-aware-web-apps-and-websites-part-1/)
> - 📖 [Building RTL-Aware Web Apps & Websites: Part 2 - Mozilla Hacks](https://hacks.mozilla.org/2015/10/building-rtl-aware-web-apps-websites-part-2/)

**[⬆ наверх](#Содержание)**

---

## Картинки

> **Примечание:** Для полного понимания оптимизации картинок прочтите бесплатную электронную книгу **[Essential Image Optimization](https://images.guide/)** от Addy Osmani.

### Лучшие практики

- [ ] **Оптимизация:** ![High][high_img] Все картинки оптимизированы для рендеринга в браузере. Формат WebP может быть использован для критических страниц, например домашняя страница (Homepage).

> - 🛠 [Imagemin](https://github.com/imagemin/imagemin)
> - 🛠 Используйте [ImageOptim](https://imageoptim.com/) для бесплатной оптимизации картинок.
> - 🛠 Используйте [Kraken.io](https://kraken.io/web-interface) как крутую альтернативу для оптимизации png и jpg. До 1 Mb бесплатно.
> - 🛠 Используйте [TinyPNG](https://tinypng.com/) для оптимизации png, apng (анимированный png) and jpg без потери качества. Есть как платная, так и бесплатная версия.
> - 🛠 [ZorroSVG](http://quasimondo.com/ZorroSVG/) jpg-подобное сжатие для прозрачных картинок использованием svg масок.
> - 🛠 [SVGO](https://github.com/svg/svgo) инструмент под Nodejs для оптимизации SVG файлов.
> - 🛠 [SVGOMG](https://jakearchibald.github.io/svgomg/) web версия SVGO для онлайн оплимизации SVG файлов.

- [ ] **Picture/Srcset:** ![Medium][medium_img] Используйте picture/srcset чтобы задать наиболее подходящую картинку для текущего viewport.

> - 📖 [How to Build Responsive Images with srcset](https://www.sitepoint.com/how-to-build-responsive-images-with-srcset/)

- [ ] **Retina:** ![Low][low_img] Вы используете картинки большего размера 2x или 3x для поддержки дисплеев retina.
- [ ] **Спрайты:** ![Medium][medium_img] Мелкие картинки объединены в спрайт файл. В случае иконок это может быть SVG файл.
- [ ] **Width и Height:** ![High][high_img] Задайте атрибуты `width` и `height` для `<img>` если размеры картинки заранее известны. Может быть пропущен для задания размеров через CSS.
- [ ] **Альтернативный текст:** ![High][high_img] Для всех `<img>` задан альтернативный текст, который описывает картинку.

> - 📖 [Alt-texts: The Ultimate Guide](https://axesslab.com/alt-texts/)

- [ ] **Ленивая загрузка (lazy loading):** ![Medium][medium_img] Применяется lazy loading для картинок (задан резервный noscript).

**[⬆ наверх](#Содержание)**

---

## JavaScript

### Лучшие практики

- [ ] **JavaScript Inline:** ![High][high_img] Не используется inline JavaScript (смешанный с HTML).
- [ ] **Конкатенация:** ![High][high_img] JavaScript файлы сконкатенированы в один.
- [ ] **Минификация:** ![High][high_img] JavaScript файлы минифицированы. Можете добавить суффикс `.min`.

> - 📖 [Minify Resources (HTML, CSS, and JavaScript)](https://developers.google.com/speed/docs/insights/MinifyResources)

- [ ] **Безопасность JavaScript:** ![High][high_img]

> - 📖 [Guidelines for Developing Secure Applications Utilizing JavaScript](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet#Guidelines_for_Developing_Secure_Applications_Utilizing_JavaScript)

- [ ] **`noscript` tag:** ![Medium][medium_img] Используйте `<noscript>` внутри `<body>` чтобы задать контент для ситуаций, когда скрипты не поддерживаются или выключены в браузере. Полезно для Single Page Application (React, Angular и т.п.)
      [Пример](https://webdesign.tutsplus.com/tutorials/quick-tip-dont-forget-the-noscript-element--cms-25498)

```html
<noscript>
  Для работы приложения необходимо включить JavaScript.
</noscript>
```

- [ ] **Неблокирующий JS:** ![Medium][medium_img] JavaScript файлы загружаются асинхронно с использованием атрибута `async` или отложенно с `defer`.

> - 📖 [Remove Render-Blocking JavaScript](https://developers.google.com/speed/docs/insights/BlockingJS)

- [ ] **Оптимизированние и актуальные версии JS библиотек:** ![Medium][medium_img] Убедитесь, что все загружаемые JS библиотеки действительно необходимы, избавьтесь от неиспользуемых. Несложный функционал предпочтительно реализовывать на чистом (vanilla) JavaScript. Используйте последние версии библиотек. В них меньше ошибок и они более безопасны по сравнению с устаревшими версиями.

> - 📖 [You may not need jQuery](http://youmightnotneedjquery.com/)
> - 📖 [Vanilla JavaScript for building powerful web applications](https://plainjs.com/)

- [ ] **Modernizr:** ![Low][low_img] С помощью кастомного Modernizr можно добавлять классы к `<html>`.

> - 🛠 [Customize your Modernizr](https://modernizr.com/download?setclasses)

### Тестирование JavaScript

- [ ] **ESLint:** ![High][high_img] ESLint не выдал ошибок, проверяя ваш код. Можно использовать ваш собственный конфиг, или стандартные правила.

> - 📖 [ESLint - The pluggable linting utility for JavaScript and JSX](https://eslint.org/)

**[⬆ наверх](#Содержание)**

---

## Безопасность

### Просканируйте и проверьте ваш веб-сайт

> - [securityheaders.io](https://securityheaders.io/)
> - [Observatory by Mozilla](https://observatory.mozilla.org/)
> - [ASafaWeb - Automated Security Analyser for ASP.NET Websites](https://asafaweb.com/)

### Лучшие практики

- [ ] **HTTPS:** ![High][high_img] HTTPS используется на всех страницах, а также для всего стороннего контента (плагины, картинки...).

> - 🛠 [Let's Encrypt - Free SSL/TLS Certificates](https://letsencrypt.org/)
> - 🛠 [Free SSL Server Test](https://www.ssllabs.com/ssltest/index.html)
> - 📖 [Strict Transport Security](http://caniuse.com/#feat=stricttransportsecurity)

- [ ] **HTTP Strict Transport Security (HSTS):** ![Medium][medium_img] Выставлен HTTP заголовок 'Strict-Transport-Security'.

> - 🛠 [Check HSTS preload status and eligibility](https://hstspreload.org/)
> - 📖 [HTTP Strict Transport Security Cheat Sheet - OWASP](https://www.owasp.org/index.php/HTTP_Strict_Transport_Security_Cheat_Sheet)
> - 📖 [Transport Layer Protection Cheat Sheet - OWASP](https://www.owasp.org/index.php/Transport_Layer_Protection_Cheat_Sheet)

- [ ] **Защита от фальсификации межсайтовых запросов(Cross Site Request Forgery - CSRF):** ![High][high_img] Вы гарантируете, что запросы на ваш сервер делаются именно вашим веб-сайтом, чтобы избежать атак CSRF.

> - 📖 [Cross-Site Request Forgery (CSRF) Prevention Cheat Sheet - OWASP](<https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF)_Prevention_Cheat_Sheet>)

- [ ] **Межсайтовый скриптинг (Cross Site Scripting - XSS):** ![High][high_img] Ваш веб-сайт защищён от уязвимостей XSS.

> - 📖 [XSS (Cross Site Scripting) Prevention Cheat Sheet - OWASP](<https://www.owasp.org/index.php/XSS_(Cross_Site_Scripting)_Prevention_Cheat_Sheet>)
> - 📖 [DOM based XSS Prevention Cheat Sheet - OWASP](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet)

- [ ] **Заголовок Content-Type:** ![Medium][medium_img] Предотвратить mime-sniff (анализ контента и подмена заголовка content-type) в Google Chrome и Internet Explorer.

> - 📖 [X-Content-Type-Options - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-content-type-options)

- [ ] **X-Frame-Options (XFO):** ![Medium][medium_img] Защитите своих пользователей от атак типа clickjacking.

> - 📖 [X-Frame-Options - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-frame-options)
> - 📖 [RFC7034 - HTTP Header Field X-Frame-Options](https://tools.ietf.org/html/rfc7034)

- [ ] **Политика безопасности контента (Content Security Policy):** ![Medium][medium_img] Задайте правила, определяющие, какой контент и откуда разрешено загружать на ваш сайт. Также это поможет защититься против атак clickjacking.

> - 📖 [Content Security Policy - An Introduction - Scott Helme](https://scotthelme.co.uk/content-security-policy-an-introduction/)
> - 📖 [CSP Cheat Sheet - Scott Helme](https://scotthelme.co.uk/csp-cheat-sheet/)
> - 📖 [CSP Cheat Sheet - OWASP](https://www.owasp.org/index.php/Content_Security_Policy_Cheat_Sheet)
> - 📖 [Content Security Policy Reference](https://content-security-policy.com/)

**[⬆ наверх](#Содержание)**

---

## Производительность

### Лучшие практики

- [ ] **Цели:** ![Medium][medium_img] Необходимо достичь следующих параметров:
  - First Meaningful Paint (показать что-то осмысленное) не позже, чем через 1 секунду
  - Time To Interactive (время до первого взаимодействия с пользователем) в течение 5 секунд для "среднего" устройства (смартфон на Android за 200\$ медленной 3G сети с 400ms RTT и скоростью передачи 400kbps) и до 2 секунд для следующих визитов
  - Размер критичных файлов до 170Kb gzipped

> - 🛠 [Website Page Analysis](https://tools.pingdom.com)
> - 🛠 [WebPageTest](https://www.webpagetest.org/)
> - 📖 [Size Limit: Make the Web lighter](https://evilmartians.com/chronicles/size-limit-make-the-web-lighter)

- [ ] **Минифицирование:** ![Medium][medium_img] Ваш HTML минифицирован.

* [ ] **Ленивая загрузка (Lazy loading):** ![Medium][medium_img] Используйте lazy loading для загрузки картинок, скриптов и CSS чтобы уменьшить время инициализации страницы. Смотрите подробнее в соответствующих секция чеклиста.

* [ ] **Размер cookie:** ![Medium][medium_img] Если используете cookies, убедитесь, что их размер не превосходит 4096 байт. Также один домен не должен использовать более 20 cookies.

> - 📖 [Cookie specification: RFC 6265](https://tools.ietf.org/html/rfc6265)
> - 📖 [Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
> - 🛠 [Browser Cookie Limits](http://browsercookielimits.squawky.net/)

- [ ] **Сторонние компоненты (Third party components):** ![Medium][medium_img] Iframe и сторонние компоненты, полагающиеся на JS с других доменов (типа кнопок "Поделиться"), должны быть, по возможности, заменены на ваши статические компоненты, дабы уменьшить число запросов и избежать возможной утечки данных ваших пользователей.

> - 🛠 [Simple sharing buttons generator](https://simplesharingbuttons.com/)

### Подготовка предстоящих запросов (preparing upcoming requests)

> - 📖 [Explanation of the following techniques](https://css-tricks.com/prefetching-preloading-prebrowsing/)

- [ ] **DNS resolution:** ![Low][low_img] DNS сторонних компонентов обозначены в `dns-prefetch`, чтобы браузер мог разобраться с этими DNS заранее.

```html
<link rel="dns-prefetch" href="https://example.com" />
```

- [ ] **Preconnect:** ![Low][low_img] Используйте `preconnect`, чтобы браузер мог осуществить DNS lookup, TCP handshake и TLS negotiation заранее во время простоя браузера.

```html
<link rel="preconnect" href="https://example.com" />
```

- [ ] **Prefetch:** ![Low][low_img] С использованием `prefetch` ресурсы, которые скоро могут понадобиться, например картинки с lazy loading, будут подгружены заранее во время простоя браузера.

```html
<link rel="prefetch" href="image.png" />
```

- [ ] **Preload:** ![Low][low_img] `preload` заранее загружает ресурсы, требуемые для текущей страницы, например скрипты в конце `<body>`.

```html
<link rel="preload" href="app.js" />
```

> - 📖 [Difference between prefetch and preload](https://medium.com/reloading/preload-prefetch-and-priorities-in-chrome-776165961bbf)

### Тестирование производительности

- [ ] **Google PageSpeed:** ![High][high_img] Все страницы протестированы и имеют рейтинг хотя бы 90/100.

> - 🛠 [Google PageSpeed](https://developers.google.com/speed/pagespeed/insights/)
> - 🛠 [Test your mobile speed with Google](https://testmysite.withgoogle.com)
> - 🛠 [WebPagetest - Website Performance and Optimization Test](https://www.webpagetest.org/)
> - 🛠 [GTmetrix - Website speed and performance optimization](https://gtmetrix.com/)

**[⬆ наверх](#Содержание)**

---

## Доступность

> **Примечание:** Ознакомьтесь с плейлистом [A11ycasts with Rob Dodson](https://www.youtube.com/playlist?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g) 📹

### Лучшие практики

- [ ] **Прогрессивное улучшение:** ![Medium][medium_img] Основной функционал, например навигация и поиск, должны работать даже если JavaScript выключен.

> - 📖 [Enable / Disable JavaScript in Chrome Developer Tools](https://www.youtube.com/watch?v=kBmvq2cE0D8)

- [ ] **Контрастность цветов:** ![Medium][medium_img] Контрастность должна соответствовать WCAG AA (AAA для мобильных устройств).

> - 🛠 [Contrast ratio](https://leaverou.github.io/contrast-ratio/)

#### Заголовки

- [ ] **H1:** ![High][high_img] На всех страницах есть H1, который отличается от title страницы.
- [ ] **Заголовки:** ![High][high_img] Заголовки должны идти в правильном порядке (от H1 к H6).

> - 📹 [Why headings and landmarks are so important -- A11ycasts #18](https://www.youtube.com/watch?v=vAAzdi1xuUY&index=9&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

### Семантика

- [ ] **Специальные типы input для HTML5:** ![Medium][medium_img] Это особенно важно для мобильных устройств, т.к. там используется разные клавиатуры для разных типов вводимых данных.

> - 📖 [Mobile Input Types](http://mobileinputtypes.com/)

### Формы

- [ ] **Label:** ![High][high_img] `<label>` задан для каждого элемента формы. Если его применить нельзя, используйте `aria-label`.

> - 📖 [Using the aria-label attribute - MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-label_attribute)

### Тестирование доступности

- [ ] **Проверка на соответствие стандартам:** ![High][high_img] Используйте инструмент WAVE для проверки.

> - 🛠 [Wave testing](http://wave.webaim.org/)

- [ ] **Клавиатурная навигация:** ![High][high_img] Пройдитесь по вашему сайту, используя только клавиатуру. Все интерактивные элементы должны быть доступны.
- [ ] **Screen-reader:** ![Medium][medium_img] Проверьте все страницы в программах для чтения экрана (screen-reader) таких как VoiceOver, ChromeVox, NVDA или Lynx.
- [ ] **Стили для фокуса:** ![High][high_img] Если фокус запрещён, к элементу под фокусом должны применяться специальные стили.

> - 📹 [Managing Focus - A11ycasts #22](https://www.youtube.com/watch?v=srLRSQg6Jgg&index=5&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

**[⬆ наверх](#Содержание)**

---

## SEO

- [ ] **Google Analytics:** ![High][high_img] Google Analytics установлен и настроен.
- [ ] **Логичные заголовки:** ![Medium][medium_img] Текст заголовков помогает понять контент страницы.
- [ ] **sitemap.xml:** ![High][high_img] sitemap.xml существует и задан в Google Search Console (ранее Google Webmaster Tools).
- [ ] **robots.txt:** ![High][high_img] robots.txt не блокирует страницы.

> - 🛠 Проверьте robots.txt с [Google Robots Testing Tool](https://www.google.com/webmasters/tools/robots-testing-tool)

- [ ] **Структурированные данные (Structured Data):** ![High][high_img] На страницах используются проверенные и правильные структурированные данные. Они помогают паукам (crawlers) понять контент страницы.

> - 📖 [Introduction to Structured Data - Search - Google Developers](https://developers.google.com/search/docs/guides/intro-structured-data)
> - 🛠 Проверьте свою страницу с [Structured Data Testing Tool](https://developers.google.com/structured-data/testing-tool/)
> - 🛠 Польный список слов, используемых в структурированных данных [Schema.org Full Heirarchy](http://schema.org/docs/full.html)
> - 📖 [RDFa - Linked Data in HTML](https://rdfa.info/)
> - 📖 [JSON-LD](https://json-ld.org/)
> - 📖 [Microdata](https://www.w3.org/TR/microdata/)

- [ ] **HTML карта сайта:** ![Medium][medium_img] HTML карта сайта существует и доступна по ссылке в подвале страницы.

> - 📖 [Sitemap guidelines - Google Support](https://support.google.com/webmasters/answer/183668?hl=en)

- [ ] **Pagination теги:** ![Medium][medium_img] Задайте `rel="prev"` и `rel="next"` чтобы показать, что контент разбит на страницы.

> - 🛠 [Pagination (rel="prev/next") Testing Tool](https://technicalseo.com/seo-tools/rel-prev-next/)

> - 📖 [Pagination guidelines - Google Support](https://support.google.com/webmasters/answer/1663744?hl=en)

```html
<!-- Example: Pagination link tags for page 2 of a paginated list -->
<link rel="prev" href="https://example.com/?page=1" />
<link rel="next" href="https://example.com/?page=3" />
```

**[⬆ наверх](#Содержание)**

---

## Перевод

Front-End Checklist также доступен на других языках. Спасибо всем переводчикам за потрясающую работу!

- 🇯🇵 Японский: [miya0001/Front-End-Checklist](https://github.com/miya0001/Front-End-Checklist)
- 🇪🇸 Испанский: [eoasakura/Front-End-Checklist-ES](https://github.com/eoasakura/Front-End-Checklist-ES)
- 🇨🇳 Китайский: [JohnsenZhou/Front-End-Checklist](https://github.com/JohnsenZhou/Front-End-Checklist)
- 🇰🇷 Корейский: [kesuskim/Front-End-Checklist](https://github.com/kesuskim/Front-End-Checklist)
- 🇧🇷 Португальский: [jcezarms/Front-End-Checklist](https://github.com/jcezarms/Front-End-Checklist)
- 🇻🇳 Вьетнамский: [euclid1990/Front-End-Checklist](https://github.com/euclid1990/Front-End-Checklist)
- 🇹🇼 Традиционный китайский: [EngineLin/Front-End-Checklist](https://github.com/EngineLin/Front-End-Checklist)
- 🇫🇷 Французский: [ynizon/Front-End-Checklist](https://github.com/ynizon/Front-End-Checklist)
- 🇷🇺 Русский: [ungear/Front-End-Checklist](https://github.com/ungear/Front-End-Checklist)
- 🇹🇷 Турецкий: [eraycetinay/Front-End-Checklist](https://github.com/eraycetinay/Front-End-Checklist)
- 🇩🇪 Немецкий: [xfuture603/Front-End-Checklist](https://github.com/xFuture603/Front-End-Checklist)
- 🇺🇦 Украинский: [antonkryvko/Front-End-Checklist](https://github.com/antonkryvko/Front-End-Checklist)

---

## Front-End Checklist Badge

Вставьте этот бейдж в ваш файл README, если хотите показать, что следуете этому чеклисту!

➔ [![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)

```md
[![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)
```

**[⬆ наверх](#Содержание)**

---

## Содействие

**Создайте issue или pull request чтобы предложить изменение или дополнение**

### Руководство

Репозиторий **Front-End Checklist** состоит из двух веток:

#### 1. `master`

Эта ветка состоит из файла `README.md`, который автоматически отображается на сайте [Front-End Checklist](http://frontendchecklist.com/).

#### 2. `develop`

Эта ветка будет использоваться для внесения значительных изменений в структуру или контент. Для устранения мелких ошибок и создания новых элементов предпочтительно использовать ветку master.

## Поддержка

Если у вас есть вопросы или пожелания, без колебаний пишите в Gitter или Twitter:

- [Chat on Gitter](https://gitter.im/Front-End-Checklist/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link)
- [Facebook](https://www.facebook.com/frontendchecklist/)
- [Twitter](https://twitter.com/thedaviddias)

## Автор

**[David Dias](https://github.com/thedaviddias)**

## Помощники

Проект существует благодаря помощи сообщества. [[Contribute]](.github/CONTRIBUTING.md).
<a href="https://github.com/thedaviddias/Front-End-Checklist/graphs/contributors"><img src="https://opencollective.com/front-end-checklist/contributors.svg?width=890" /></a>

## Backers

Thank you to all our backers! 🙏 [[Become a backer](https://opencollective.com/front-end-checklist#backer)]

<a href="https://opencollective.com/front-end-checklist#backers" target="_blank"><img src="https://opencollective.com/front-end-checklist/backers.svg?width=890"></a>

## Sponsors

Support this project by becoming a sponsor. Your logo will show up here with a link to your website. [[Become a sponsor](https://opencollective.com/front-end-checklist#sponsor)]

<a href="https://opencollective.com/front-end-checklist/sponsor/0/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/0/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/1/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/1/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/2/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/2/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/3/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/3/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/4/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/4/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/5/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/5/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/6/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/6/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/7/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/7/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/8/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/8/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/9/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/9/avatar.svg"></a>

## Лицензия

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

**[⬆ наверх](#Содержание)**

[low_img]: https://raw.githubusercontent.com/thedaviddias/Front-End-Checklist/master/data/images/priority/low.svg
[medium_img]: https://raw.githubusercontent.com/thedaviddias/Front-End-Checklist/master/data/images/priority/medium.svg
[high_img]: https://raw.githubusercontent.com/thedaviddias/Front-End-Checklist/master/data/images/priority/high.svg.svg

Syncronized with commit 225705b3bb4c7b05a6f818203b408575fe240473
