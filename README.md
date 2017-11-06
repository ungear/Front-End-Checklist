# Front-End Checklist

[![Join the chat at https://gitter.im/Front-End-Checklist/Lobby](https://badges.gitter.im/Front-End-Checklist/Lobby.svg)](https://gitter.im/Front-End-Checklist/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)
[![Contributors](https://img.shields.io/github/contributors/thedaviddias/Front-End-Checklist.svg)](https://github.com/thedaviddias/Front-End-Checklist/graphs/contributors)
[![StackShare](https://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/thedaviddias/front-end-checklist)
[![CC0](https://img.shields.io/badge/license-CC0-green.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

**Front-End Checklist** - это исчерпывающий список элементов сайта или HTML страницы, которые должны быть проверены перед выпуском в production.

Он основан на многолетнем опыте front-end разработчиков и, кроме того, включает в себя части других открытых checklist-ов.

*Проголосуй или порекомендуй Front-End Checklist на платформе Product Hunt чтобы помочь с продвижением.*
[![](http://res.cloudinary.com/djnyaloac/image/upload/v1508896898/upvote-producthunt_vzys4c.jpg)](https://www.producthunt.com/posts/front-end-checklist)

## Содержание

1. **[Head](#head)**
2. **[HTML](#html)**
3. **[Webfonts](#webfonts)**
4. **[CSS](#css)**
5. **[Картинки](#images)**
6. **[JavaScript](#javascript)**
7. **[Безопасность](#security)**
8. **[Производительность](#performance-1)**
9. **[Доступ](#accessibility)**
10. **[SEO](#seo)**

## Как этим пользоваться?

Все пункты **Front-End Checklist** обязательны для большинства сайтов, однако некоторые элементы могут быть менее важны или вовсе пропущены (например если вам не нужен RSS для админки проложения). Мы выбрали 3 уровня гибкости:

* ![Low][low_img] означает, что пункт **рекомендован**, но может быть пропущен в некоторых случаях.
* ![Medium][medium_img] элемент **крайне рекомендован** и можен быть пропущен только в очень специфических ситуациях. Невыполнение некоторых пунктов может иметь негативные последствия, например с точки производительности или SEO.
* ![High][high_img] такой пункт **обязателен**. Может сломать страницу или привести к проблемам с доступом и SEO. Проверяйте такие элементы в первую очередь.

Некоторые комментарии снабжены иконками, чтобы вы лучше понимали, какой контент или помощь можно найти:

* 📖: документация или статья
* 🛠: он-лайн инструменты / утилиты для проверки
* 📹: медиа или видео контент

---

## Head

> **Примечание:** Можно посмотреть [список всего](https://github.com/joshbuchea/HEAD), что может быть в `<head>` HTML документа.

### Мета-теги

* [ ] **Doctype:** ![High][high_img] Doctype отностится к HTML5 и находится в самом верху HTML страниц.

```html
<!-- Doctype HTML5 -->
<!doctype html>
```

> * 📖 [Определение кодировки (англ.) - HTML5 W3C](https://www.w3.org/TR/html5/syntax.html#determining-the-character-encoding)

*Следующие 3 мета-тега (Charset, X-UA Compatible and Viewport) должны быть расположены в самом начале `<head>`.*

* [ ] **Charset:** ![High][high_img] Кодировка (UTF-8) задана правильно.

```html
<!-- Задать кодировку документа -->
<meta charset="utf-8">
```

* [ ] **X-UA-Compatible:** ![Medium][medium_img] Тег X-UA-Compatible присутствует.

```html
<!-- Проинструктировать Internet Explorer использовать последний движок рендеринга -->
<meta http-equiv="x-ua-compatible" content="ie=edge">
```

> * 📖 [Задать режим совместимости Internet Explorer (англ.)](https://msdn.microsoft.com/en-us/library/jj676915(v=vs.85).aspx)

* [ ] **Viewport:** ![High][high_img] Viewport задан правильно.

```html
<!-- Задать viewport для responsive дизайна -->
<meta name="viewport" content="width=device-width, initial-scale=1">
```

* [ ] **Title:** ![High][high_img] Задан на всех страницах (SEO: Google рассчитывает ширину символов в title и обрезает примерно от 472 до 482 пикселей. Так что предел длины title около 55 символов).

```html
<!-- Document Title -->
<title>Название короче 55 символов</title>
```

> * 📖 [Title - HTML - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title)
> * 🛠 [SERP Snippet Generator](https://www.sistrix.com/serp-snippet-generator/)

* [ ] **Description:** ![High][high_img] Description задан, уникален и короче 150 символов.

```html
<!-- Meta Description -->
<meta name="description" content="Описание страницы короче 150 символов">
```

> * 📖[Meta Description - HTML - MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#Adding_an_author_and_description)

* [ ] **Favicons:** ![Medium][medium_img] Иконки отображаются корректно. Если у вас только один `favicon.ico`, положите его в корень сайта. Обычно вам не нужно ничего добавлять в разметку. Однако, хорошей практикой считается сделать ссылку как в примере ниже. На сегодняшний день **рекомендован PNG формат** вместо `.ico`(разрешение: 32x32px).

```html
<!-- Стандартный favicon -->
<link rel="icon" type="image/x-icon" href="https://example.com/favicon.ico">
<!-- Рекомендованный формат favicon -->
<link rel="icon" type="image/png" href="https://example.com/favicon.png">
```

> * 🛠 [Favicon Generator](https://www.favicon-generator.org/)
> * 🛠 [RealFaviconGenerator](https://realfavicongenerator.net/)
> * 📖 [Favicon шпаргалка](https://github.com/audreyr/favicon-cheat-sheet)
> * 📖 [Favicons, Touch Icons, Tile Icons, etc. Which Do You Need? - CSS Tricks](https://css-tricks.com/favicon-quiz/)
> * 📖 [PNG favicons - caniuse](https://caniuse.com/#feat=link-icon-png)

* [ ] **Apple Touch Icon:** ![Low][low_img] Иконка для Apple задана с помощью apple-mobile-web-app-capable *(Создайте файл Apple Icon с разрешением как минимум 200x200px для поддержки всех разрешений, которые могут вам понадобиться).*

```html
<!-- Apple Touch Icon -->
<link rel="apple-touch-icon" href="/custom-icon.png">
```

> * 📖 [Configuring Web Applications](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)

- [ ] **Windows Tiles:**![Low][low_img] Windows tiles заданы.

```html
<!-- Microsoft Tiles -->
<meta name="msapplication-config" content="browserconfig.xml" />
```

Минимальный требуемый browserconfig.xml:

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

> * 📖 [Browser configuration schema reference](https://msdn.microsoft.com/en-us/library/dn320426(v=vs.85).aspx)

* [ ] **Canonical:** ![Medium][medium_img] Используйте `rel="canonical"` чтобы избежать дублированности контента.

```html
<!-- Помогает избежать проблем с дублированным контентом -->
<link rel="canonical" href="http://example.com/2017/09/a-new-article-to-red.html">
```

> * 📖 [Use canonical URLs - Search Console Help - Google Support](https://support.google.com/webmasters/answer/139066?hl=en)
> * 📖 [5 common mistakes with rel=canonical - Google Webmaster Blog](https://webmasters.googleblog.com/2013/04/5-common-mistakes-with-relcanonical.html)

### HTML теги

* [ ] **Атрибут lang:** ![High][high_img] Атрибут `lang` задан в соответствии с языком страницы.

```html
<html lang="en">
```

* [ ] **Атрибут direction:** ![Medium][medium_img] Направление текста задано в этом атрибуте тега `html`. Также этот атрибут может быть применён к другим тегам.

```html
<html dir="rtl">
```

> * 📖 [dir - HTML - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/dir)

* [ ] **Альтернативный язык:** ![Low][low_img] Тег языка задан и соответствует языку страницы.

```html
<link rel="alternate" href="https://es.example.com/" hreflang="es">
```

* [ ] **Условные комментарии:** ![Low][low_img] Условные комментарии заданы для IE, если требуется.

> * 📖 [About conditional comments (Internet Explorer) - MSDN - Microsoft](https://msdn.microsoft.com/en-us/library/ms537512(v=vs.85).aspx)

* [ ] **RSS feed:** ![Low][low_img] Если ваш проект является блогом или содержит страницы, убедитесь, что RSS настроен.

* [ ] **Критичные CSS стили заданы inline:** ![Medium][medium_img] Критичный CSS (critical CSS) - CSS, задающий стили контента видимого сразу же пока идёт процесс загрузки страницы ("above the fold content"). Минифицируйте такой CSS и вставьте внутри `<style></style>` перед загрузкой остальных стилей.
> * 🛠 Инструмент для автомизации: [Critical by Addy Osmani on GitHub](https://github.com/addyosmani/critical)

* [ ] **Порядок CSS:** ![High][high_img] Все CSS файлы должны загружаться перед любыми JavaScript файлами в `<head>`. (За исключением случаев, когда JS файлы загружаются асинхронно в верху страницы).

### Социальные сети

***Facebook OG*** и ***Twitter Cards*** крайне рекомендованы для всех сайтов. Рассмотрите теги для других соц. сетей, если планируете отображаться в них коретно.

* [ ] **Facebook Open Graph:** ![Low][low_img] Все теги All Facebook Open Graph (OG) протестированы, ни один не пропущен и информация в них верна. Картинки должны быть хотя бы 600 x 315 пикселей. Рекомендуемое разрешение 1200 x 630 пикселей.

> **Примечание:** Используйте `og:image:width` и `og:image:height` чтобы указать разрешение картинок для паука (the crawler) для того, чтобы картинки могли быть отрендерены сразу же. Иначе потребуется асинхронная подгрузка и обработка.

```html
<meta property="og:type" content="website">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<!-- Следующие теги не обязательны, но рекомендованы -->
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
```

> * 📖 [A Guide to Sharing for Webmasters](https://developers.facebook.com/docs/sharing/webmasters/)
> * 📖 [Best Practices - Sharing](https://developers.facebook.com/docs/sharing/best-practices/)
> * 🛠 Протестируйте страницу с [Facebook OG testing](https://developers.facebook.com/tools/debug/)

* [ ] **Twitter Card:** ![Low][low_img]

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
```

> * 📖 [Getting started with cards — Twitter Developers](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/guides/getting-started)
> * 🛠 Проверьте страницу с [Twitter card validator](https://cards-dev.twitter.com/validator)

**[⬆ наверх](#table-of-contents)**

---

## HTML

### Лучшие практики

* [ ] **Семантические элементы HTML5:** ![High][high_img] Семантические элементы HTML5 используются должным образом (header, section, footer, main...).

> * 📖 [HTML Reference](http://htmlreference.io/)

* [ ] **Страницы ошибок:** ![High][high_img] Страницы ошибок 404 и 5xx существуют. Не забывайте, что в страницы ошибок 5xx должны быть включены их стили, чтобы обойтись без подгрузки с сервера.

* [ ] **Noopener:** ![Medium][medium_img] Ссылки на внешние ресурсы с `target="_blank"` должы иметь атрибут `rel="noopener"`, чтобы предотвратить фишинговые атаки типа tab nabbing. Если нужно поддерживать старие версии Firefox, используйте `rel="noopener noreferrer"`.

> * 📖 [About rel=noopener](https://mathiasbynens.github.io/rel-noopener/)

* [ ] **Удаление комментариев:** ![Low][low_img] Ненужный код должен быть удалён перед отправкой в production.

### Тестирование HTML

* [ ] **W3C совместимость:** ![High][high_img] Все страницы должны быть проверены W3C валидатором.

> * 🛠 [W3C validator](https://validator.w3.org/)

* [ ] **HTML Lint:** ![High][high_img] Инструменты, которые помогают анализировать проблены в HTML.

> * 🛠 [Dirty markup](https://dirtymarkup.com/)

> * 🛠 [Sonar a linting tool for the web](https://sonarwhal.com/)

* [ ] **Проверка ссылок:** ![High][high_img] Нет сломанных ссылок, нет ошибок 404.

> * 🛠 [W3C Link Checker](https://validator.w3.org/checklink)

* [ ] **Проверка на Adblock:** ![Medium][medium_img] Сайт коррекрно отображается c включёнными вырезателями рекламы типа Adblock. Можете показать специальное сообщение с просьбой выключить подобные плагины.



**[⬆ наверх](#table-of-contents)**

---

## Web-шрифты

> **Примечание:** Использование web-шрифтов может вызвать мерцание или исчезновение текста (FOUT - Flash of Unstyled Text, FOIT - Flash of Invisible Text). Так что убедитесь, что задан резервный шрифт, либоо используйте загрузчик шрифтов чтобы держать ситуацию под контролем.
> * 📖 [Google Technical considerations about webfonts](https://developers.google.com/fonts/docs/technical_considerations)

* [ ] **Форматы web-шрифтов:** ![High][high_img] WOFF, WOFF2 и TTF поддерживаются всеми браузерами.

> * 📖 [WOFF - Web Open Font Format - Caniuse](https://caniuse.com/#feat=woff).
> * 📖 [WOFF 2.0 - Web Open Font Format - Caniuse](https://caniuse.com/#feat=woff2).
> * 📖 [TTF/OTF - TrueType and OpenType font support](https://caniuse.com/#feat=ttf)
> * 📖 [Using @font-face - CSS-Tricks](https://css-tricks.com/snippets/css/using-font-face/)

* [ ] **Размер web-шрифтов:** ![High][high_img] Размер шрифтов суммарно не превышает 2 MB.

* [ ] **Заргузчик web-шрифтов:** ![Low][low_img] Контролируйте закачку шрифтов с помощью загрузчика.

> * 🛠 [Typekit Web Font Loader](https://github.com/typekit/webfontloader)

**[⬆ наверх](#table-of-contents)**

---

## CSS

> **Примечание:** Ознакомьтесь с [CSS guidelines](https://cssguidelin.es/) и [Sass Guidelines](https://sass-guidelin.es/), которых придерживаются большинство разработчиков. Если у вас есть сомнения насчёт CSS свойств, посетите [CSS Reference](http://cssreference.io/). Кроме того взгляните на короткий гайд [Code Guide](http://codeguide.co/).

* [ ] **Отзывчивый (responsive) веб-дизайн:** ![High][high_img] Дизайн должен быть отзывчивым.
* [ ] **CSS для печати:** ![Medium][medium_img] Стили для печати заданы и работают корректны.
* [ ] **Препоцессоры:** ![Low][low_img] Используются препроцессоры, [Sass](http://sass-lang.com/) рекомендуется.
* [ ] **Уникальные ID:** ![High][high_img] Если используются Id, убедитесь, что они уникальны в пределах страницы.
* [ ] **Сброс (reset) CSS:** ![High][high_img] Используются актуальные версии инструментов для нормализации CSS (reset, normalize or reboot). *(Если используете CSS фреймворк типа Bootstrap или Foundation, Normalize уже в них включён.)*

> * 📖 [Reset.css](https://meyerweb.com/eric/tools/css/reset/)
> * 📖 [Normalize.css](https://necolas.github.io/normalize.css/)
> * 📖 [Reboot](https://getbootstrap.com/docs/4.0/content/reboot/)

* [ ] **JS префиксы:** ![Low][low_img] Все классы и id, используемые в JS файлах, начинаются с префикса **js-** и не учавствуют в назначении стилей.

```html
<div id="js-slider" class="my-slider">
<!-- Или -->
<div id="id-used-by-cms" class="js-slider my-slider">
```

* [ ] **Embedded или inline CSS:** ![High][high_img] Любой ценой избегайти внедрения CSS в `<style>` теги (embeding) или inline стилей. Применяйте такие подходы только в особых случаях, например background-image для слайдера или critical CSS (см. выше).
* [ ] **Вендорные префиксы:** ![High][high_img] CSS вендорные префиксы используются и генерируются в соответствии с поддерживаемыми браузерами.

> * 🛠 [Autoprefixer CSS online](https://autoprefixer.github.io/)

### Производительность

- [ ] **Конкатенация:** ![High][high_img] CSS фыйлы сконкатенированы в один файл *(Не для HTTP/2)*.
- [ ] **Минификация:** ![High][high_img] Все CSS файлы минифицированы.
- [ ] **Неблокирующий CSS:** ![Medium][medium_img] CSS файлы должны быть неблокирующими DOM, чтобы избежать потерь времени.

> * 📖 [loadCSS by filament group](https://github.com/filamentgroup/loadCSS)
> * 📖 [Example of preload CSS using loadCSS](https://gist.github.com/thedaviddias/c24763b82b9991e53928e66a0bafc9bf)

- [ ] **Неиспользуемый CSS:** ![Low][low_img] Удалите неиспользуемые стили.

> * 🛠 [UnCSS Online](https://uncss-online.com/) 🛠
> * 🛠 [PurifyCSS](https://github.com/purifycss/purifycss)
> * 🛠 [Chrome DevTools Coverage](https://developers.google.com/web/updates/2017/04/devtools-release-notes#coverage)


### Тестирование CSS

* [ ] **Stylelint:** ![High][high_img] В CSS или SCSS файлах нет ошибок.

> * 🛠 [stylelint, a CSS linter](https://stylelint.io/)
> * 📖 [Sass guidelines](https://sass-guidelin.es/)

* [ ] **Отзывчивый web-дизайн:** ![High][high_img] Все страницы были протестированы на следующих контрольных точках: 320px, 768px, 1024px (может быть больше а зависимости от проекта).

* [ ] **CSS валидатор:** ![Medium][medium_img] CSS был протестирован, ошибки исправлены.

> * 🛠 [CSS Validator](https://jigsaw.w3.org/css-validator/)

* [ ] **Desktop браузеры:** ![High][high_img] Все страницы были протестированы на всех поддерживаемых desktop браузерах (Safari, Firefox, Chrome, Internet Explorer, EDGE...).
* [ ] **Мобильные браузеры:**  ![High][high_img] Все страницы были протестированы на всех поддерживаемых мобильных браузерах (Native browser, Chrome, Safari...).
* [ ] **ОС:**  ![High][high_img] Все страницы были протестированы на всех поддерживаемых ОС (Windows, Android, iOS, Mac...).

- [ ] **Pixel perfect:** ![High][high_img] Все страницы выполнены с пиксельной точностью. В зависимости от качества макета, вы можете не достигнуть 100% соответствия, но к этому нужно стремиться.

> [Pixel Perfect - Chrome Extension](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en)

* [ ] **Направление текста:** ![High][high_img] Все страницы должны быть протестированы в LTR и RTL языках, если они поддерживаются.

> * 📖 [Building RTL-Aware Web Apps & Websites: Part 1 - Mozilla Hacks](https://hacks.mozilla.org/2015/09/building-rtl-aware-web-apps-and-websites-part-1/)
> * 📖 [Building RTL-Aware Web Apps & Websites: Part 2 - Mozilla Hacks](https://hacks.mozilla.org/2015/10/building-rtl-aware-web-apps-websites-part-2/)

**[⬆ наверх](#table-of-contents)**

---

## Картинки

> **Примечание:** Для полного понимания оптимизации картинок прочтимте бесплатную электронную книгу **[Essential Image Optimization](https://images.guide/)** от Addy Osmani.

### Лучшие практики

* [ ] **Оптимизация:** ![High][high_img] Все картинки оптимизированы для рендеринга в браузере. Формат WebP может быть использован для критических страниц, например домашняя страница (Homepage).

> * 🛠 [Imagemin](https://github.com/imagemin/imagemin)
> * 🛠 Используйти [ImageOptim](https://imageoptim.com/) для бесплатной оптимизации картинок.
> * 🛠 Используйте [Kraken.io](https://kraken.io/web-interface) как крутую альтернативу для оптимизации png и jpg. До 1 Mb бесплатно.

* [ ] **Picture/Srcset:** ![Medium][medium_img] Используйте picture/srcset чтобы задать наиболее подходящую картинку для текущего viewport.

> * 📖 [How to Build Responsive Images with srcset](https://www.sitepoint.com/how-to-build-responsive-images-with-srcset/)

* [ ] **Retina:** ![Low][low_img] Вы используете картинки большего размера 2x или 3x для поддержки дисплеев retina.
* [ ] **Спрайты:** ![Medium][medium_img] Мелкие картинки объединены в спрайт файл. В случае иконок это может быть SVG файл.
* [ ] **Width и Height:** ![High][high_img] Задайте атрибуты `width` и `height` для `<img>` если размеры картинки заранее известны. Может быть пропущен для задания размеров через CSS.
* [ ] **Альтернативный текст:** ![High][high_img] Для всех `<img>` задан альтернативный текст, который описывает картинку.

> * 📖 [Alt-texts: The Ultimate Guide](https://axesslab.com/alt-texts/)

* [ ] **Ленивая загрузка (lazy loading):** ![Medium][medium_img] Применяется lazy loading для картинок (задан резервный noscript).

**[⬆ наверх](#table-of-contents)**

---

## JavaScript

### Лучшие практики

* [ ] **JavaScript Inline:** ![High][high_img] Не используется inline JavaScript (смешанный с HTML).
* [ ] **Конкатенация:** ![High][high_img] JavaScript файлы сконкатенированы в один.
* [ ] **Минификация:** ![High][high_img] JavaScript файлы минифицированы. Можете добавить суффикс `.min`.

> * 📖 [Minify Resources (HTML, CSS, and JavaScript)](https://developers.google.com/speed/docs/insights/MinifyResources)

* [ ] **Безопасность JavaScript:**

> * 📖 [Guidelines for Developing Secure Applications Utilizing JavaScript](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet#Guidelines_for_Developing_Secure_Applications_Utilizing_JavaScript)

* [ ] **Неблокирующий JS:** ![Medium][medium_img] JavaScript файлы загружаются астнхрогго с использованием `async` или отложенно с `defer` аорибутом.

> * 📖 [Remove Render-Blocking JavaScript](https://developers.google.com/speed/docs/insights/BlockingJS)

* [ ] **Modernizr:** ![Low][low_img] If you need to target some specific features you can use a custom Modernizr to add classes in your `<html>` tag.

> * 🛠 [Customize your Modernizr](https://modernizr.com/download?setclasses)

### JavaScript testing

* [ ] **ESLint:** ![High][high_img] No errors are flagged by ESLint (based on your configuration or standards rules).

> * 📖 [ESLint - The pluggable linting utility for JavaScript and JSX](https://eslint.org/)

**[⬆ наверх](#table-of-contents)**

---

## Security

### Scan and check your web site

> * [securityheaders.io](https://securityheaders.io/)
> * [Observatory by Mozilla](https://observatory.mozilla.org/)
> * [ASafaWeb - Automated Security Analyser for ASP.NET Websites](https://asafaweb.com/)

### Best practices

* [ ] **HTTPS:** ![Medium][medium_img] HTTPS is used on every pages and for all external content (plugins, images...).

> * 🛠 [Let's Encrypt - Free SSL/TLS Certificates](https://letsencrypt.org/)
> * 🛠 [Free SSL Server Test](https://www.ssllabs.com/ssltest/index.html)
> * 📖 [Strict Transport Security](http://caniuse.com/#feat=stricttransportsecurity)

* [ ] **HTTP Strict Transport Security (HSTS):** ![Medium][medium_img] The HTTP header is set to 'Strict-Transport-Security'.

> * 🛠 [Check HSTS preload status and eligibility](https://hstspreload.org/)
> * 📖 [HTTP Strict Transport Security Cheat Sheet - OWASP](https://www.owasp.org/index.php/HTTP_Strict_Transport_Security_Cheat_Sheet)
> * 📖 [Transport Layer Protection Cheat Sheet - OWASP](https://www.owasp.org/index.php/Transport_Layer_Protection_Cheat_Sheet)

* [ ] **Cross Site Request Forgery (CSRF):** ![High][high_img] You ensure that requests made to your server-side are legitimate and originate from your website / app to prevent CSRF attacks.

> * 📖 [Cross-Site Request Forgery (CSRF) Prevention Cheat Sheet  - OWASP](https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF)_Prevention_Cheat_Sheet)

* [ ] **Cross Site Scripting (XSS):** ![High][high_img] Your page or website is free from XSS possible issues.

> * 📖 [XSS (Cross Site Scripting) Prevention Cheat Sheet  - OWASP](https://www.owasp.org/index.php/XSS_(Cross_Site_Scripting)_Prevention_Cheat_Sheet)
> * 📖 [DOM based XSS Prevention Cheat Sheet  - OWASP](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet)

* [ ] **Content Type Options** ![Medium][medium_img] Prevents Google Chrome and Internet Explorer from trying to mime-sniff the content-type of a response away from the one being declared by the server.

> * 📖 [X-Content-Type-Options - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-content-type-options)

* [ ] **X-Frame-Options (XFO)** ![Medium][medium_img] Protects your visitors against clickjacking attacks.

> * 📖 [X-Frame-Options - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-frame-options)
> * 📖 [RFC7034 - HTTP Header Field X-Frame-Options](https://tools.ietf.org/html/rfc7034)

* [ ] **Content Security Policy** ![Medium][medium_img] Defines how content is loaded on your site and from where it is permitted to be loaded. Can also be used to protect against clickjacking attacks.

> * 📖 [Content Security Policy - An Introduction - Scott Helme](https://scotthelme.co.uk/content-security-policy-an-introduction/)
> * 📖 [CSP Cheat Sheet - Scott Helme](https://scotthelme.co.uk/csp-cheat-sheet/)
> * 📖 [CSP Cheat Sheet - OWASP](https://www.owasp.org/index.php/Content_Security_Policy_Cheat_Sheet)

**[⬆ наверх](#table-of-contents)**

---

## Performance

### Best practices

- [ ] **Page weight:** ![High][high_img] The weight of each page is between 0 and 500 KB.

> * 🛠 [Website Page Analysis](https://tools.pingdom.com)
> * 📖 [Size Limit: Make the Web lighter](https://evilmartians.com/chronicles/size-limit-make-the-web-lighter)

- [ ] **Minified:** ![Medium][medium_img] Your HTML is minified.
> * 🛠 [W3C Validator](https://validator.w3.org/)

* [ ] **Lazy loading:** ![Medium][medium_img] Images, scripts and CSS need to be lazy loaded to improve the response time of the current page (See details in their respective sections).

* [ ] **Cookie size:** If you are using cookies be sure each cookie doesn't exceed 4096 bytes and your domain name doesn't have more than 20 cookies.

> * 📖 [Cookie specification: RFC 6265](https://tools.ietf.org/html/rfc6265)
> * 📖 [Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
> * 🛠 [Browser Cookie Limits](http://browsercookielimits.squawky.net/)

* [ ] **Third party components:** ![Medium][medium_img] Third party iframes or components relying on external JS (like sharing buttons) are replaced by static components when possible, thus limiting calls to external APIs and keeping your users activity private.

> * 🛠 [Simple sharing buttons generator](https://simplesharingbuttons.com/)

### Preparing upcoming requests

> * 📖 [Explanation of the following techniques](https://css-tricks.com/prefetching-preloading-prebrowsing/)

* [ ] **DNS resolution:** ![Low][low_img] DNS of third-party services that may be needed are resolved in advance during idle time using `dns-prefetch`.

```html
<link rel="dns-prefetch" href="https://example.com">
```

* [ ] **Preconnection:** ![Low][low_img] DNS lookup, TCP handshake and TLS negotiation with services that will be needed soon is done in advance during idle time using `preconnect`.

```html
<link rel="preconnect" href="https://example.com">
```

* [ ] **Prefetching:** ![Low][low_img] Resources that will be needed soon (e.g. lazy loaded images) are requested in advance during idle time using `prefetch`.

```html
<link rel="prefetch" href="image.png">
```

* [ ] **Preloading:** ![Low][low_img] Resources needed in the current page (e.g. scripts placed at the end of `<body>`) in advance using `preload`.

```html
<link rel="preload" href="app.js">
```

> * 📖 [Difference between prefetch and preload](https://medium.com/reloading/preload-prefetch-and-priorities-in-chrome-776165961bbf)

### Performance testing

* [ ] **Google PageSpeed:** ![High][high_img] All your pages were tested (not only the homepage) and have a score of at least 90/100.

> * 🛠 [Google PageSpeed](https://developers.google.com/speed/pagespeed/insights/)
> * 🛠 [Test your mobile speed with Google](https://testmysite.withgoogle.com)
> * 🛠 [WebPagetest - Website Performance and Optimization Test](https://www.webpagetest.org/)
> * 🛠 [GTmetrix - Website speed and performance optimization](https://gtmetrix.com/)

**[⬆ наверх](#table-of-contents)**

---

## Accessibility

> **Примечание:** You can watch the playlist [A11ycasts with Rob Dodson](https://www.youtube.com/playlist?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g) 📹

### Best practices

- [ ] **Progressive enhancement:** ![Medium][medium_img] Major functionality like main navigation and search should work without JavaScript enabled.

> * 📖 [Enable / Disable JavaScript in Chrome Developer Tools](https://www.youtube.com/watch?v=kBmvq2cE0D8)

- [ ] **Color contrast:** ![Medium][medium_img] Color contrast should at least pass WCAG AA (AAA for mobile).

> * 🛠 [Contrast ratio](https://leaverou.github.io/contrast-ratio/)

#### Headings

* [ ] **H1:** ![High][high_img] All pages have an H1 which is not the title of the website.
* [ ] **Headings:** ![High][high_img] Headings should be used properly in the right order (H1 to H6).

> * 📹 [Why headings and landmarks are so important -- A11ycasts #18](https://www.youtube.com/watch?v=vAAzdi1xuUY&index=9&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

#### Landmarks

- [ ] **Role banner:** ![High][high_img] `<header>` has `role="banner"`.
- [ ] **Role navigation:** ![High][high_img] `<nav>` has `role="navigation"`.
- [ ] **Role main:** ![High][high_img] `<main>` has `role="main"`.

> * 📖 [Using ARIA landmarks to identify regions of a page](https://www.w3.org/WAI/GL/wiki/Using_ARIA_landmarks_to_identify_regions_of_a_page)
> * 📖 [ARIA roles categorization](https://www.w3.org/TR/wai-aria/roles#roles_categorization)

### Semantics

- [ ] **Specific HTML5 input types are used:** ![Medium][medium_img] This is especially important for mobile devices that show customized keypads and widgets for different types.

> * 📖 [Mobile Input Types](http://mobileinputtypes.com/)

### Form

* [ ] **Label:** ![High][high_img] A label is associated with each input form element. In case a label can't be displayed, use `aria-label` instead.

> * 📖 [Using the aria-label attribute - MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-label_attribute)

### Accessibility testing

* [ ] **Accessibility standards testing:** ![High][high_img] Use the WAVE tool to test if your page respects the accessibility standards.

> * 🛠 [Wave testing](http://wave.webaim.org/)

* [ ] **Keyboard navigation:** ![High][high_img] Test your website using only your keyboard in a previsible order. All interactive elements are reachable and usable.
* [ ] **Screen-reader:** ![Medium][medium_img] All pages were tested in a screen-reader (VoiceOver, ChromeVox, NVDA or Lynx).
* [ ] **Focus style:** ![High][high_img] If the focus is disabled, it is replaced by visible state in CSS.

> * 📹 [Managing Focus - A11ycasts #22](https://www.youtube.com/watch?v=srLRSQg6Jgg&index=5&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

**[⬆ наверх](#table-of-contents)**

---

## SEO

* [ ] **Google Analytics:** ![High][high_img] Google Analytics is installed and correctly configured.
* [ ] **Headings logic:** ![Medium][medium_img] Heading text helps to understand the content in the current page.
* [ ] **sitemap.xml:** ![High][high_img] A sitemap.xml exists and was submitted to Google Search Console (previously Google Webmaster Tools).
* [ ] **robots.txt:** ![High][high_img] The robots.txt is not blocking webpages.

> * 🛠 Test your robots.txt with [Google Robots Testing Tool](https://www.google.com/webmasters/tools/robots-testing-tool)

* [ ] **Structured Data:** ![High][high_img] Pages using structured data are tested and are without errors. Structured data helps crawlers understand the content in the current page.

> * 📖 [Introduction to Structured Data - Search - Google Developers](https://developers.google.com/search/docs/guides/intro-structured-data)
> * 🛠 Test your page with the [Structured Data Testing Tool](https://developers.google.com/structured-data/testing-tool/)
> * 🛠 Complete list of vocabularies that can be used as structured data. [Schema.org Full Heirarchy](http://schema.org/docs/full.html)

* [ ] **Sitemap HTML:** ![Medium][medium_img] An HTML sitemap is provided and is accessible via a link in the footer of your website.

> * 📖 [Sitemap guidelines - Google Support](https://support.google.com/webmasters/answer/183668?hl=en)
> * 🛠 [Sitemap generator](https://websiteseochecker.com/html-sitemap-generator/)

**[⬆ наверх](#table-of-contents)**

---

## Translation

The Front-End Checklist is also available in other languages. Thanks for all translators and their awesome work!

* 🇯🇵 Japanese: [miya0001/Front-End-Checklist](https://github.com/miya0001/Front-End-Checklist)
* 🇪🇸 Spanish: [eoasakura/Front-End-Checklist-ES](https://github.com/eoasakura/Front-End-Checklist-ES)
* 🇨🇳 Chinese: [JohnsenZhou/Front-End-Checklist](https://github.com/JohnsenZhou/Front-End-Checklist)
* 🇰🇷 Korean: [kesuskim/Front-End-Checklist](https://github.com/kesuskim/Front-End-Checklist)
* 🇧🇷 Portuguese: [jcezarms/Front-End-Checklist](https://github.com/jcezarms/Front-End-Checklist)
* 🇻🇳 Vietnamese: [euclid1990/Front-End-Checklist](https://github.com/euclid1990/Front-End-Checklist)
* 🇹🇼 Traditional Chinese: [EngineLin/Front-End-Checklist](https://github.com/EngineLin/Front-End-Checklist)

---

## Front-End Checklist Badge

If you want to show you are following the rules of the Front-End Checklist, put this badge on your README file!

➔ [![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)

```md
[![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)
```

**[⬆ наверх](#table-of-contents)**

---

## Contributing

**Open an issue or a pull request to suggest changes or additions.**

### Guide

The **Front-End Checklist** repository consists of two branches:

#### 1. `master`

This branch consists of the `README.md` file that is automatically reflected on the [Front-End Checklist](http://frontendchecklist.com/) website.

#### 2. `develop`

This branch will be used to make some significant changes to the structure, content if needed. It is preferable to use the master branch to fix small errors or add a new item.

### Contributors

Check out all the super awesome [contributors](https://github.com/thedaviddias/frontendchecklist/graphs/contributors).

## Support

If you have any question or suggestion, don't hesitate to use Gitter or Twitter:

* [Chat on Gitter](https://gitter.im/Front-End-Checklist/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link)
* [Facebook](https://www.facebook.com/frontendchecklist/)
* [Twitter](https://twitter.com/thedaviddias)

## Authors

**[David Dias](https://github.com/thedaviddias/Front-End-Checklist)**

## License

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

**[⬆ наверх](#table-of-contents)**

[low_img]: http://res.cloudinary.com/djnyaloac/image/upload/v1508238836/level-checklist-low.png
[medium_img]: http://res.cloudinary.com/djnyaloac/image/upload/v1508238836/level-checklist-medium.png
[high_img]: http://res.cloudinary.com/djnyaloac/image/upload/v1508238836/level-checklist-high.png
