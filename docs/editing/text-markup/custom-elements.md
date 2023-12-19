# Дополнительные элементы

### **idea**

Элемент `idea` используется для выделения текста, который представляет собой самостоятельную мысль, идею или посыл, и который может быть цитирован в подходящем контексте.

```html
<idea>Гурудев имел обыкновение говорить: «Что-то лучше чем ничего».</idea>
```

### **\_ (подчёркивание)**

Символ нижнего подчёркивания используется для обозначеня пар слов, которые всегда должны оставаться на одной строке. Он преобразуется в HTML-последовательность `&nbsp;` («non breaking space» — неразрывный пробел).

```html
Эта_строка_будет_отображена_без_переносов.
```

### **nowrap**

Элемент `nowrap` предназначен для обозначения текста, который должен отображаться без переносов.

```html
<nowrap>Этот текст будет отображаться одной строкой без переносов, что может привести к появлению горизонтальной полосы прокрутки.</nowrap>
```

Отличие от элемента `_` состоит в том, что `nowrap` можно применять к любым последовательностям символов.

```html
<nowrap>5-летний</nowrap> мальчик
```