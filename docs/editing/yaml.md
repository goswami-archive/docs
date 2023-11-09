# Заголовок YAML («YAML front matter»)

Помимо разметки самого текста, часто бывает необходимо хранить в документе техническую информацию о самом документе (например язык содержимого, дату создания, автора и т.д.). Для таких целей хорошо зарекомендовал себя подход с использованием вступительной части на [YAML](https://ru.wikipedia.org/wiki/YAML). Такой подход широко используется во многих статических генераторах Web-сайтов (Jekyll, Hugo, Assemble, Eleventy).

Разметка YAML основана на пробелах и переносах строк. YAML-документ состоит из полей (пар ключ-значение), располагающихся на отдельных строках. Допускаеться неограниченная вложенность полей. Для обозначения вложенности необходимо более 1 пробела (для читаемости рекомендуется 2 и более). Более подробное описание синтаксиса [YAML](https://www.cloudbees.com/blog/yaml-tutorial-everything-you-need-get-started).

### **Общие правила YAML**

* YAML-документ отделяется тремя дефисами в начале и в конце;
* пары ключ-значение располагаются на отделных строках;
* табы запрещены;
* комментарии начинаются с символа `#`.

**Пример**

```yaml
---
type: post
title: О Сарасвати Тхакуре
authors: 
  - Бхакти Судхир Госвами
date: 2012-02-12
lang: ru
location: Чианг Май
audio: https://youtube/?watch=...
image: 
  desktop: sarswati-thakur.jpg
  alt: Сарсвати Тхакур с учениками
slug: ru-2012-02-12-about-saraswati-thakur
tags:
  - Сарасвати Тхакур
translators:
  - Амия Синдху Дас
transcribers:
  - Амия Синдху Дас
---
```

### **Поддерживаемые поля**

<table><thead><tr><th width="182">Ключ</th><th width="146" align="center">Тип значения</th><th width="128" align="center">Обязательное</th><th>Описание</th></tr></thead><tbody><tr><td><code>type</code></td><td align="center">строка</td><td align="center">✔</td><td>Допустимые значения: <code>post</code>, <code>category</code>, <code>playlist</code>.</td></tr><tr><td><code>title</code></td><td align="center">строка</td><td align="center">✔</td><td>Название лекции, статьи, книги. Используйте двойные кавычки если название содержит специальные символы YAML: <code>,</code> <code>!</code> <code>:</code>.</td></tr><tr><td><code>authors</code></td><td align="center">список</td><td align="center">✔</td><td>Авторы текста, или спикеры.</td></tr><tr><td><code>date</code></td><td align="center">строка</td><td align="center"></td><td>Дата записи аудио, публикации статьи в формате <code>гггг-мм-дд</code></td></tr><tr><td><code>lang</code></td><td align="center">строка</td><td align="center">✔</td><td>Язык содержимого (2-имвольный код в стандарте <a href="https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes">ISO 639-1</a>)</td></tr><tr><td><code>description</code></td><td align="center">строка</td><td align="center"></td><td>SEO-описание, не больше 200 символов.</td></tr><tr><td><code>draft</code></td><td align="center">логическое (true/false)</td><td align="center"></td><td><code>draft: true</code> означает, что текст не готов к публикации</td></tr><tr><td><code>location</code></td><td align="center">строка</td><td align="center"></td><td>Место записи лекции (город, страна).</td></tr><tr><td><code>audio</code></td><td align="center">строка</td><td align="center"></td><td>URL аудиозаписи, или относительный путь к локальному файлу.</td></tr><tr><td><code>video</code></td><td align="center">строка</td><td align="center"></td><td>URL видеозаписи, или относительный путь к локальному файлу.</td></tr><tr><td><code>editors</code></td><td align="center">список</td><td align="center"></td><td>Редакторы.</td></tr><tr><td><code>translators</code></td><td align="center">список</td><td align="center"></td><td>Список переводчиков.</td></tr><tr><td><code>transcribers</code></td><td align="center">список</td><td align="center"></td><td>Список создателей транскрипции.</td></tr><tr><td><code>image</code></td><td align="center">обьект</td><td align="center"></td><td><p>Описание изображения, которое может применяться в качестве изображения записи. Обьект с ключами:</p><ul><li><code>desktop</code>: изображение для больших экранов </li><li><code>mobile</code>: изображение для маленьких экранов</li><li><code>alt</code>: <a href="https://htmlacademy.ru/blog/html/alt-text">алтернативный текст</a></li></ul></td></tr><tr><td><code>slug</code></td><td align="center">строка</td><td align="center"></td><td>Уникальная строка идентификатор, которая будет отображаться в URL страницы (в <a href="https://medium.com/@alivander/camel-pascal-snake-case-%D0%B8-%D0%B4%D1%80%D1%83%D0%B3%D0%B8%D0%B5-%D1%81%D1%82%D0%B8%D0%BB%D0%B8-%D0%BD%D0%B0%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D1%8F-288ec62ca0d0">kebab-case</a>).</td></tr><tr><td><code>tags</code></td><td align="center">список</td><td align="center"></td><td>Список тегов.</td></tr></tbody></table>

#### `type`&#x20;

_Строка._

Тип сущности. Допустимые значения: `post`, `category`, `playlist`.

#### `title`

_Строка_.

Название лекции, статьи, книги. Используйте двойные кавычки если название содержит специальные символы YAML: `,` `!` `:`.

#### `authors`&#x20;

_Список._

Авторы текста, или спикеры.

#### `date`&#x20;

_Строка._

Дата записи аудио, публикации статьи в формате `гггг-мм-дд`.

#### `description`&#x20;

_Строка._

SEO-описание, не больше 200 символов.

#### `lang`&#x20;

_Строка._

Язык содержимого, 2-имвольный код в стандарте [ISO 639-1](https://en.wikipedia.org/wiki/List\_of\_ISO\_639-1\_codes).

#### `draft`&#x20;

_Строка (_`true`, `false`)

`draft: true` означает, что текст не готов к публикации.

#### `location`&#x20;

_Строка._

Место записи лекции (город, страна).

#### `audio`&#x20;

_Строка._

URL аудиозаписи, или относительный путь к локальному файлу.

#### `video`&#x20;

_Строка._

URL видеозаписи, или относительный путь к локальному файлу.

#### `editors`&#x20;

_Список._

Список редакторов.

```yaml
---
editors:
  - John Doe
  - Simon Peters
---
```

#### `translators`&#x20;

_Список._

Список переводчиков.

```yaml
---
translators:
  - John Doe
  - Simon Peters
---
```

#### `transcribers`&#x20;

_Список._

Список создателей транскрипции.

```yaml
---
transcribers:
  - John Doe
  - Simon Peters
---
```

#### `image`&#x20;

_Обьект._

Описание изображения, которое может применяться в качестве изображения записи:

* `desktop`: изображение для больших экранов&#x20;
* `mobile`: изображение для маленьких экранов
* `alt`: [алтернативный текст](https://htmlacademy.ru/blog/html/alt-text)

```yaml
---
image: 
  desktop: sarswati-thakur.jpg
  alt: Сарсвати Тхакур с учениками
---
```

#### `slug`&#x20;

_Строка._

Уникальная строка идентификатор, которая будет отображаться в URL страницы (в [kebab-case](https://medium.com/@alivander/camel-pascal-snake-case-%D0%B8-%D0%B4%D1%80%D1%83%D0%B3%D0%B8%D0%B5-%D1%81%D1%82%D0%B8%D0%BB%D0%B8-%D0%BD%D0%B0%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D1%8F-288ec62ca0d0)).

#### `tags`&#x20;

_Список._

Список тегов.

```yaml
---
tags:
  - tag 1
  - tag 2
---
```

### Поля для типа "post"

* [type](yaml.md#type) (обязательное)
* [title](yaml.md#title) (обязательное)
* [authors](yaml.md#authors) (обязательное)
* [lang](yaml.md#lang) (обязательное)
* [date](yaml.md#date)
* lang
* description
*

