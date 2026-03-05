# Archive structure

Archive has 2 main directories:

* `content` - root for all content;
* `tools` - scripts for managing archive content (download, lint, search, rename etc.)

### Content

Archive content is grouped by following types:

* `audios`
* `playlists`
* `articles`
* `books`

### :open\_file\_folder: `audios`

This directory contains all audio lectures.

Most of the lectures are grouped by year. Others are grouped by source. 
This grouping represents a kind of categorization. 
Category directory usually contains Markdown file with category metadata at it's root.

Each lecture is stored in a separate directory.
At a simpliest case this directory may contain single Markdown file. 
This file contains information on a lecture, transcription, and a path to local audio file or URL of a remote file.
The structure of Markdown file is described in the ["Document structure"](../working-with-documents/document-structure/) section.

`audios` section has the following structure:

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

This directory contains all articles.
Articles are grouped by year. Each article is stored in a dedicated directory.

```txt
year
  date_Article_Title
    lang1_date_Article_Title.md
    lang2_date_Article_Title.md
```

### :open\_file\_folder: playlists

This directory stores playlists in Markdown format.

```text
Playlist_Title
  lang1_Playlist_Title.md
  lang1_Playlist_Title.jpg
  lang2_Playlist_Title.md
  lang2_Playlist_Title.jpg
```

### :open\_file\_folder: books

This directory contains all books.

```text
year_Book_Title
  lang1_year_Book_Title.pdf
  lang2_year_Book_Title.pdf
```
