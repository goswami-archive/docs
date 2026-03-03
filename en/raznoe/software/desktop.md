# Программы для десктопа

### Sublime Text 3

* [Скачать](https://www.sublimetext.com/3).
* [Неофициальная документация](https://sublime-text-unofficial-documentation.readthedocs.io/en/sublime-text-2/index.html).

#### Конфигурация

* включите настройку _View_ -> _Word Wrap_;
* убедитесь что выставлен синтаксис **HTML**: вызовите `Command Pallette` (`ctrl + shift + p`), введите _"syntax html"_, выберите _"Set Syntax: HTML"_ и нажмите `Enter`.

#### Сниппеты

Набор сниппетов и "горячих клавиш" для разметки согласно руководству.

{% file src="../../.gitbook/assets/sublime_text_snippets.zip" %}

#### **Установка**

Распакуйте содержимое архива в папку `Data/Packages/User`. Расположение папки `Data` зависит от платформы:

* **Windows:** `%APPDATA%\Sublime Text 3`
* **macOS:** `~/Library/Application Support/Sublime Text 3`
* **Linux:** `~/.config/sublime-text-3`
* Для portable-установок: `Sublime Text 3/Data`

#### **Использование**

Использовать сниппеты можно несколькими способами:

1. При создании текста:
   * ввести триггер-последовательность (или её часть) и нажать ctrl + space, затем в выпавшем меню выбрать нужный сниппет;
   * вызвать `Command Pallette` (ctrl + shift + p), ввести название сниппета (для удобства все сниппеты содержат текст "Goswami" в названии), и затем выбрать нужный сниппет;
2. При редактировании текста: выделите нужный фрагмент и нажмите комбинацию горячих клавиш - текст будет обёрнут в соответствующий тег.

Многие сниппеты содержат внутри себя "контрольные точки", по которым можно перемещаться клавишей Tab после вставки сниппета.

**Таблица маппинга сниппетов и горячих клавиш**

| Сниппет                     |   Tab-триггер   |    Windows / Linux   |           macOS          |
| --------------------------- | :-------------: | :------------------: | :----------------------: |
| `<h></h>`                   |        h        | `ctrl` + `alt` + `h` | `option` + `shift` + `h` |
| `<i></i>`                   |        i        | `ctrl` + `alt` + `i` | `option` + `shift` + `i` |
| `<em></em>`                 |        em       | `ctrl` + `alt` + `e` | `option` + `shift` + `e` |
| `<b></b>`                   |        b        | `ctrl` + `alt` + `b` | `option` + `shift` + `b` |
| `<blockquote></blockquote>` |    blockquote   | `ctrl` + `alt` + `q` | `option` + `shift` + `q` |
| `<abbr></abbr>`             |       abbr      | `ctrl` + `alt` + `a` | `option` + `shift` + `a` |
| `<time></time>`             |       time      | `ctrl` + `alt` + `t` | `option` + `shift` + `t` |
| `#::#`                      |     timecode    | `ctrl` + `alt` + `3` | `option` + `shift` + `3` |
| `<fn></fn>`                 |        fn       | `ctrl` + `alt` + `f` | `option` + `shift` + `f` |
| `<anno></anno>`             |       anno      | `ctrl` + `alt` + `n` | `option` + `shift` + `n` |
| `<idea></idea>`             |       idea      | `ctrl` + `alt` + `d` | `option` + `shift` + `d` |
| —                           |      emdash     | `ctrl` + `alt` + `-` |                          |
| –                           |      endash     | `ctrl` + `alt` + `=` |                          |
| …                           |      ellip      | `ctrl` + `alt` + `.` |                          |
| ’                           |  apostrophe-en  | `ctrl` + `alt` + `'` |                          |
| «»                          | quotes-ru-outer | `ctrl` + `alt` + `1` |                          |
| „“                          | quotes-ru-inner | `ctrl` + `alt` + `2` |                          |
| “”                          | quotes-en-outer | `ctrl` + `alt` + `[` |                          |
| ‘’                          | quotes-en-inner | `ctrl` + `alt` + `]` |                          |

### Visual Studio Code

...
