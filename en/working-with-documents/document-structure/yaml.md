# YAML Front Matter

It's ofter necessary to store technical information about the document itself (e.g. language, creation date, author and so on) in addition to the text. For such purposes YAML Front Matter is a good choice. It is widely used in static site generators (Jekyll, Hugo, Assemble, Eleventy).

See Wikipedias's [YAML](https://ru.wikipedia.org/wiki/YAML) page for more information.

YAML markup is based on spaces and line breaks. YAML document consists of fields (key-value pairs) located on separate lines. It is allowed to have unlimited nesting of fields. For indicating nesting it is necessary to have more than 1 space (for readability it is recommended to use 2 or more). More detailed description of the syntax can be found [here](https://www.cloudbees.com/blog/yaml-tutorial-everything-you-need-get-started).

## Basic YAML rules

* YAML document is separated by three dashes in the beginning and in the end;
* pairs of keys-values are located on separate lines;
* tabs are forbidden;
* comments start with `#`.

**Example**

```yaml
---
type: post
title: "About Saraswati Thakur"
authors: 
  - Bhakti Sudhar Gosvami
date: 2012-02-12
lang: en
location: "Chiang Mai, Thailand"
audio: https://youtube/?watch=...
image: 
  desktop: sarswati-thakur.jpg
  alt: Saraswati Thakur with disciples
slug: en-2012-02-12-about-saraswati-thakur
tags:
  - Saraswati Thakur
translators:
  - Amiya Sindhu Das
transcribers:
  - Amiya Sindhu Das
---
```

## Entity Types

Following types are used in the YAML front matter:
* `post` - used for audio lectures and articles;
* `category` - categories;
* `playlist` - playlists.

### `post` fields

* [type](yaml.md#type) (required)
* [title](yaml.md#title) (required)
* [authors](yaml.md#authors) (required)
* [lang](yaml.md#lang) (required)
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

### `category` and `playlist` fields

* [type](yaml.md#type) (required)
* [title](yaml.md#title) (required)
* [lang](yaml.md#lang) (required)
* [description](yaml.md#description)
* [image](yaml.md#image)
* [slug](yaml.md#slug)

**Example**

```yaml
---
type: category
title: 2012
lang: en
image: 
  desktop: en_2012.jpg
---
```

### Fields description

#### `type`

_String._ (values: `post`, `category`, `playlist`)

Entity type.

#### `title`

_String_.

Entity title. Use double quotes to preserve special characters.

#### `authors`

_List_.

Speakers or authors of the text.

#### `date`

_String._

Date of audio recording or publication of the article in the format `YYYY-MM-DD`.

#### `description`

_String._

SEO description. Maximum 200 characters. Uuse double quotes to preserve special characters.

#### `lang`

_String._

Content language, 2-letter code in the [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) standard.

#### `status`

_String_. (values: `draft`, `publish`)

Content status.

#### `location`

_String._

Place where a lecture was recorded.

#### `audio`

_Object._

Object storing references to audio files. 
Each key is a human readable source of the file and value is path to local file or URL.
Path is relative to markdown file.
There is always at least one `file` key, which points to the audio file itself.

**Example**
```yaml
audio:
  file: en_2012-02-12_About_Saraswati_Thakur.mp3
  youtube: https://youtube/?watch=...
  vimeo: https://vimeo/?watch=...
```

#### `video`

_String._

URL видеозаписи, или относительный путь к локальному файлу.

#### `editors`

_List_.

Список редакторов.

```yaml
---
editors:
  - John Doe
  - Simon Peters
---
```

#### `translators`

_List_.

Список переводчиков.

```yaml
---
translators:
  - John Doe
  - Simon Peters
---
```

#### `transcribers`

_List_.

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

_String._

Уникальная String идентификатор, которая будет отображаться в URL страницы (в [kebab-case](https://medium.com/@alivander/camel-pascal-snake-case-%D0%B8-%D0%B4%D1%80%D1%83%D0%B3%D0%B8%D0%B5-%D1%81%D1%82%D0%B8%D0%BB%D0%B8-%D0%BD%D0%B0%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D1%8F-288ec62ca0d0)).

#### `tags`&#x20;

_List_.

Список тегов.

```yaml
---
tags:
  - tag 1
  - tag 2
---
```

