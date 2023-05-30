# Заголовок YAML («YAML front matter»)

Помимо разметки самого текста, часто бывает необходимо хранить в документе техническую информацию о самом документе (например язык содержимого, дату создания, автора и т.д.). Для таких целей хорошо зарекомендовал себя подход с использованием вступительной части на [YAML](https://ru.wikipedia.org/wiki/YAML). Такой подход широко используется во многих статических генераторах Web-сайтов (Jekyll, Hugo, Assemble, Eleventy).

Разметка YAML основана на пробелах и переносах строк. YAML-документ состоит из полей (пар ключ-значение), располагающихся на отдельных строках. Допускаеться неограниченная вложенность полей. Для обозначения вложенности необходимо более 1 пробела (для читаемости рекомендуется 2 и более). Более подробное описание синтаксиса [YAML](https://www.cloudbees.com/blog/yaml-tutorial-everything-you-need-get-started).

**Общие правила YAML**

* YAML-документ отделяется тремя дефисами в начале и в конце;
* пары ключ-значение располагаются на отделных строках;
* табы запрещены;
* комментарии начинаются с символа `#`.

**Пример**

```yaml
---
title: О Сарасвати Тхакуре
authors: 
  - Бхакти Судхир Госвами
date: 2012-02-12
lang: ru
location: Чианг Май
audio: https://youtube/?watch=...
image: 
  lg: sarswati-thakur.jpg
  alt: Saraswati Thakur with disciples
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

<table><thead><tr><th width="182">Ключ</th><th width="149">Тип значения</th><th width="190">Обязятельное поле</th><th>Описание</th></tr></thead><tbody><tr><td><code>title</code></td><td>строка</td><td>✔</td><td>Название лекции, статьи, книги. Используйте двойные кавычки если название содержит специальные символы YAML: <code>,</code> <code>!</code> <code>:</code>.</td></tr><tr><td><code>authors</code></td><td>перечисление</td><td>✔</td><td>Авторы текста, или спикеры.</td></tr><tr><td><code>date</code></td><td>строка</td><td></td><td>Дата записи аудио, публикации статьи (формат: гггг-мм-дд).</td></tr><tr><td><code>lang</code></td><td>строка</td><td>✔</td><td>Язык содержимого (2-имвольный код в стандарте <a href="https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes">ISO 639-1</a>)</td></tr><tr><td><code>description</code></td><td>строка</td><td></td><td>SEO-описание, 160-200 символов.</td></tr><tr><td><code>location</code></td><td>строка</td><td></td><td>Место записи лекции (город, страна).</td></tr><tr><td><code>audio</code></td><td>строка</td><td></td><td>URL аудиозаписи, или относительный путь к локальному файлу.</td></tr><tr><td><code>video</code></td><td>строка</td><td></td><td>URL видеозаписи, или относительный путь к локальному файлу.</td></tr><tr><td><code>editors</code></td><td>перечисление</td><td></td><td>Редакторы.</td></tr><tr><td><code>translators</code></td><td>перечисление</td><td></td><td>Список переводчиков.</td></tr><tr><td><code>transcribers</code></td><td>перечисление</td><td></td><td>Список создателей транскрипции.</td></tr><tr><td><code>image</code></td><td>обьект</td><td></td><td><p>Описание изображения, которое может применяться в качестве изображения записи. Обьект с ключами:</p><ul><li><code>lg</code>: изображение для больших экранов</li><li><code>md</code>: изображение для средних экранов</li><li><code>sm</code>: изображение для маленьких экранов</li><li><code>alt</code>: <a href="https://htmlacademy.ru/blog/html/alt-text">алтернативный текст</a></li></ul></td></tr><tr><td><code>slug</code></td><td>строка</td><td></td><td>URL-адрес страницы в <a href="https://medium.com/@alivander/camel-pascal-snake-case-%D0%B8-%D0%B4%D1%80%D1%83%D0%B3%D0%B8%D0%B5-%D1%81%D1%82%D0%B8%D0%BB%D0%B8-%D0%BD%D0%B0%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D1%8F-288ec62ca0d0">kebab-case</a></td></tr><tr><td><code>tags</code></td><td>перечисление</td><td></td><td>Список тегов</td></tr><tr><td><code>draft</code></td><td>логическое (true/false)</td><td></td><td><code>draft: true</code> или его отсутствие означает, что текст готов к публикации</td></tr></tbody></table>

