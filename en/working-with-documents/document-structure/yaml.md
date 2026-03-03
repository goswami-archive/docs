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
title: "О Сарасвати Тхакуре"
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

#### `type`&#x20;

_Строка._

Тип сущности. Допустимые значения: `post`, `category`, `playlist`.

#### `title`

_Строка_.

Название лекции, статьи, книги. Оборачивайте в двойные кавычки.

#### `authors`&#x20;

_Список._

Авторы текста, или спикеры.

#### `date`&#x20;

_Строка._

Дата записи аудио, публикации статьи в формате `гггг-мм-дд`.

#### `description`&#x20;

_Строка._

SEO-описание, не больше 200 символов. Оборачивайте в двойные кавычки

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
* [description](yaml.md#description)
* [draft](yaml.md#draft)
* [location](yaml.md#location)
* [audio](yaml.md#audio)
* [video](yaml.md#video)
* [editors](yaml.md#editors)
* [translators](yaml.md#translators)
* [transcribers](yaml.md#transcribers)
* [tags](yaml.md#tags)
* [image](yaml.md#image)
* [slug](yaml.md#slug)

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

### Поля для типа "category", "playlist"

* [type](yaml.md#type) (обязательное)
* [title](yaml.md#title) (обязательное)
* [lang](yaml.md#lang) (обязательное)
* [description](yaml.md#description)
* [image](yaml.md#image)
* [slug](yaml.md#slug)

```yaml
---
type: category
title: 2012
lang: ru
image: 
  desktop: ru_2012.jpg
---
```
