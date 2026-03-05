# Naming conventions

## Directories

Directories are grouping multiple translations of the same entity (lecture, article, etc.). The name of the directory is the same entity title, but omitting the language prefix.

```text
2011-11-21_Deep_Feelings_of_the_Devotees
  ru_2011-11-21_Deep_Feelings_of_the_Devotees.mp3
  ru_2011-11-21_Deep_Feelings_of_the_Devotees.md
  en_2011-11-21_Deep_Feelings_of_the_Devotees.mp3
  en_2011-11-21_Deep_Feelings_of_the_Devotees.md
```

## Files

Follow next template for naming audio and text files:

```text
lang_date_Title_of_the_Entity.mp3
lang_date_Title_of_the_Entity.md
```

**Example:**

```text
ru_2011-11-21_Deep_Feelings_of_the_Devotees.mp3
ru_2011-11-21_Deep_Feelings_of_the_Devotees.md
```

* Language is specified in 2-letter code in [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) standard.
* Date is in `YYYY-MM-DD` format.
* Follow these rules for entity title:
  * use only latin alphabet characters. Do not use punctuation and other special characters - comma, dash, apostrophe and so on;
  * do not use transliteration;
  * separate words with underscore;
  * capitalize each word title except of adverbs, prepositions and so on;
* Metadata/transcription file extension is `.md` ([Markdown](../working-with-documents/semantics.md#markdown)).

If the content is divided into several parts - the part number is specified in the following format:

```text
lang_date_p{number}_Title_of_the_Entity
```

**Example:**

```text
ru_2011-01-08_p1_Copernican_Revolution.mp3
ru_2011-01-08_p2_Copernican_Revolution.mp3
```