# Archive structure

Archive has 2 main directories:

* `content` - root for all content;
* `tools` - scripts for managing archive content (download, lint, search, rename etc.)

### Content

Archive content is splitted into next groups:

<table>
  <thead>
    <tr>
      <th width="125">Directory</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>audios</code></td>
      <td>Stores all audio lectures.</td>
    </tr>
    <tr>
      <td><code>playlists</code></td>
      <td>Stores playlists information in Markdown format</td>
    </tr>
    <tr>
      <td><code>articles</code></td>
      <td>Stores articles</td>
    </tr>
    <tr>
      <td><code>books</code></td>
      <td>Stores books</td>
    </tr>
  </tbody>
</table>

### :open\_file\_folder: audios

Most of the lectures are grouped by year. Others are grouped by source.

Each lecture is represented by a directory.
At a simpliest case this directory may contain only the Markdown file. 
This file contains information on a lecture, transcription, and a path to local audio file or URL of a remote file.
The structure of Markdown file is described in the ["Document structure"](../working-with-documents/document-structure/) section.

Section has the following structure:

```text
year
  date_Lecture_Title
    lang1_date_Lecture_Title.mp3
    lang1_date_Lecture_Title.md
    lang2_date_Lecture_Title.mp3
    lang2_date_Lecture_Title.md

  date_p1_Lecture_Title
    lang_date_p1_Lecture_Title.mp3
    lang_date_p1_Lecture_Title.md

  date_p2_Lecture_Title
    lang_date_p2_Lecture_Title.mp3
    lang_date_p2_Lecture_Title.md

```

**Example:**

```text
2011
  en_2011.md
  ru_2011.md
  en_2011_cover.jpg
  ru_2011_cover.jpg

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
