# Archive structure

Archive has 2 main directories:

* `content` - root for all content;
* `tools`  - scripts for managing archive content (download, lint, search, rename etc.)

### Content

Archive content is splitted into next groups:&#x20;

<table><thead><tr><th width="128.05859375">Directory</th><th>Description</th></tr></thead><tbody><tr><td><code>audios</code></td><td>Contains all audio lectures (audio and transcription)</td></tr><tr><td><code>playlists</code></td><td>Stores playlists information</td></tr><tr><td><code>articles</code></td><td>Stores articles</td></tr><tr><td><code>books</code></td><td>Stoes books</td></tr></tbody></table>

### :open\_file\_folder: audios

Раздел содержит аудиозаписи и их текстовые расшифровки (транскрипции). Раздел также может содержать дополнительные материалы, например обложки аудио, описание раздела и т.д.

Файлы `.md` содержат транскрипцию соответстующих аудио-файлов. Структура файла описана в разделе ["Структура документа"](../working-with-documents/document-structure/).

Раздел имеет следующую структуру:

```
год
  дата_Название_Лекции
    язык1_дата_Название_Лекции.mp3
    язык1_дата_Название_Лекции.md
    язык2_дата_Название_Лекции.mp3
    язык2_дата_Название_Лекции.md

  дата_p1_Название_Лекции
    язык_дата_p1_Название_Лекции.mp3
    язык_дата_p1_Название_Лекции.md

  дата_p2_Название_Лекции
    язык_дата_p2_Название_Лекции.mp3
    язык_дата_p2_Название_Лекции.md
```

**Пример:**

```
2011
  en_2011_cover.jpg
  ru_2011_cover.jpg
  en_2011.md
  ru_2011.md

  2011-11-21_Deep_Feelings_of_the_Devotees
    en_2011-11-21_Deep_Feelings_of_the_Devotees.mp3
    en_2011-11-21_Deep_Feelings_of_the_Devotees.md
    ru_2011-11-21_Deep_Feelings_of_the_Devotees.mp3
    ru_2011-11-21_Deep_Feelings_of_the_Devotees.md

  2011-01-08_p1_Copernican_Revolution
    en_2011-01-08_p1_Copernican_Revolution.mp3
    en_2011-01-08_p1_Copernican_Revolution.md

  2011-01-08_p2_Copernican_Revolution
    en_2011-01-08_p2_Copernican_Revolution.mp3
    en_2011-01-08_p2_Copernican_Revolution.md
```

### :open\_file\_folder: articles

Раздел содержит статьи и имееет следующую структуру:

```
год
  дата_Название_Статьи
    язык1_дата_Название_Статьи.md
    язык2_дата_Название_Статьи.md
```

### :open\_file\_folder: books

Раздел содержит книги и имееет следующую структуру:

```
год
  год_название
    язык1_год_Название_Книги.pdf
    язык2_год_Название_Книги.pdf
```
