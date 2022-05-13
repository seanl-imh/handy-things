# Markdown Sample Page

The intention of this document is to provide clarity and standardize internal
documentation written in Markdown.

- [Markdown Sample Page](#markdown-sample-page)
  - [Line wrapping](#line-wrapping)
  - [Titles and Headings](#titles-and-headings)
  - [Lists](#lists)
    - [Definition lists](#definition-lists)
    - [Numbered Lists](#numbered-lists)
  - [Emphasis](#emphasis)
  - [Strikethrough](#strikethrough)
  - [Blockquotes](#blockquotes)
  - [Inline Code](#inline-code)
  - [Code Blocks](#code-blocks)
  - [Horizontal rules](#horizontal-rules)
  - [Links](#links)
    - [Inline Links](#inline-links)
    - [Automatic Hyperlinks](#automatic-hyperlinks)
    - [Image Links](#image-links)

## Line wrapping

`wrap:inner-sentence`

## Titles and Headings

Markdown defines multiple methods for section titles and headers. For our purposes
the `header:atx` method is preferred. Headings are indicated by starting the line
with one or more `#` marks with the number of `#` determining heading depth within
the document outline. Headings up to level 6 (`######`) are supported.

```text
# Level 1 (H1) Heading
## Level 2 (H2) Heading
...
###### Level 6 (H6) Heading
```

## Lists

`list-marker:hyphen`

Bullet (unordered) lists should be preceded by a hyphen (`-`) followed by a space.
Nested lists are indented 2 spaces for each nesting level. Additionally, the entire
list must be preceded and followed by a blank line.

```text
- Fruit
  - Orange
  - Peach
    - Cling
- Cake
```

- Fruit
  - Orange
  - Peach
    - Cling
- Cake

### Definition lists

Formatted lists are preferred for item definition:

- The item should be defined as either bold, link or code.
- Separate the item from the definition with a colon and a space `:.`
- Don't align definitions

Simple example:

```text
- **apple**: red fruit
- **dog**: bark bark
```

* **apple**: red fruit
* **dog**: bark bark

Multi-line definition example:

- **apple**: red fruit  
  Shiny  
  Very tasty
- **dog**: bark bark  
  Arf  
  Not tasty

### Numbered Lists

Numbered lists are renumbered sequentially upon render. For example:

```text
1. Fruit
   1. Orange
   2. Pear
5. Cake
```

Will be rendered as:

1. Fruit
   1. Orange
   1. Pear
1. Cake

It is acceptable to utilize this feature for short lists such as above, however,
for readability it is a good idea to maintain list item numbers in the source
Markdown.

Numbered lists can also be nested by using more leading space than the prior
list item.

Paragraphs can be properly nested within lists by indenting to the same level as
the first list item:

```text
1. Fruit

   In botany, a fruit is the seed-bearing structure in flowering
   plants.
 
   In common language usage, "fruit" normally means the fleshy
   seed-associated structures of a plant that are sweet or sour, and
   edible in the raw state, such as apples, bananas, grapes, lemons,
   oranges, and strawberries.

2. Cake

   The cake is a lie.
```

## Emphasis

Emphasize paragraph text with _italic_ and **bold** styles.

```text
Emphasize paragraph text with _italic_ and **bold** text.
```
<!-- -->
```text
**It is _strongly_ encouraged to review documentation for typos**
```

**It is _strongly_ encouraged to review documentation for typos**

## Strikethrough

Text can be ~~struck out~~ within a paragraph:

```text
Text can be ~~struck out~~ within a paragraph.
```

## Blockquotes

Used to stand off text obtained from another source:

```text
In the immortal words of Socrates:

> I drank _**what**_?
```

In the immortal words of Socrates:

> I drank _**what**_?

## Inline Code

Use `backticks` to markup inline code within a paragraph:

```text
Use `backticks` to markup inline code within a paragraph.
```

## Code Blocks

Multi-line spans, commands with output and other preformatted text should utilize
**unindented** fenced code blocks:

```text
Optionally specify language to enable syntax highlighting:

    ``` c
    #include <stdio.h>
    
    int main() {
      printf("Hello, World.\n");
      return 0;
    }
    ```
```

``` c
#include <stdio.h>

int main() {
  printf("Hello, World.\n");
  return 0;
}
```

## Horizontal rules

No.

[Exception](https://cirosantilli.com/markdown-style-guide/#end-of-a-header)

Use `---`

## Links

### Inline Links

```text
[Text Bar](https://example.foo)
```

[Github](https://github.com)

### Automatic Hyperlinks

Wrap automatic links in angle brackets `<https://github.com>`: <https://github.com>

### Image Links

Same format as inline links. Preceded with `!` to denote image reference:

```text
![diffy the kung fu review cuckoo](https://commondatastorage.googleapis.com/gerrit-static/diffy-w200.png)
```

![diffy the kung fu review cuckoo](https://commondatastorage.googleapis.com/gerrit-static/diffy-w200.png)
