# Markdown Sample Page

The intention of this document is to provide clarity and standardize internal
documentation written in Markdown.

TOC

## Titles and Headings

Markdown defines multiple methods for section titles and headers. For our purposes
the `header:atx` method is preferred. Headings are indicated by starting the line
with one or more `#` marks with the number of `#` determining heading depth within
the document outline. Headings up to level 6 (`######`) are supported.

```
# Level 1 (H1) Heading
## Level 2 (H2) Heading
### Level 3 (H3) Heading
#### Level 4 (H4) Heading
##### Level 5 (H5) Heading
###### Level 6 (H6) Heading
```

## Lists

`list-marker:hyphen`

Bullet (unordered) lists should be preceded by a hyphen (`-`) followed by a space.
Nested lists are indented 2 spaces for each nesting level. Additionally, the entire
list must be preceded and followed by a blank line.

```
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
- Separate the item from the definition with a colon and a space `: .`
- Don't align definitions

Simple example:

```
- **apple**: red fruit
- **dog**: bark bark
```

- **apple**: red fruit
- **dog**: bark bark

Multi-line definition example:

- **apple**: red fruit
  
    Very tasty

- **dog**: bark bark

    Not tasty

### Numbered Lists

Numbered lists are renumbered sequentially upon render. For example:

```
1. Fruit
   1. Orange
   2. Pear
5. Cake
```

Will be rendered as:

1. Fruit
   1. Orange
   2. Pear
5. Cake

It is acceptable to utilize this feature for short lists such as above, however,
for readability it is a good idea to maintain list item numbers in the source 
Markdown.

Numbered lists can also be nested by using more leading space than the prior list item.

Paragraphs can be properly nested within lists by indenting to the same level as
the first list item:

```
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

Emphasize paragraph text with *italic* and **bold** styles.

    Emphasize paragraph text with *italic* and **bold** text.
<!-- -->
    **It is *strongly* encouraged to review documentation for typos**


**It is *strongly* encouraged to review documentation for typos**

## Strikethrough

Text can be ~~struck out~~ within a paragraph:

    Text can be ~~struck out~~ within a paragraph.


## Blockquotes

Used to stand off text obtained from another source:

```
In the immortal words of Socrates:

> I drank _**what**_?
```

In the immortal words of Socrates:

> I drank _**what**_?

## Inline Code

Use `backticks` to markup inline code within a paragraph:

    Use `backticks` to markup inline code within a paragraph.

## Code Blocks

Multi-line spans, commands with output and other preformatted text should utilize
**unindented** fenced code blocks:

    Optionally specify language to enable syntax highlighting:

    ``` c
    #include <stdio.h>
    
    int main() {
      printf("Hello, World.\n");
      return 0;
    }
    ```

``` c
#include <stdio.h>

int main() {
  printf("Hello, World.\n");
  return 0;
}
```

Single line commands with no output can be indented 4 spaces and surrounded by 
one empty line. 

Prefer to end the preceding phrase with a colon `:`

    single line, no output? 4 space indent

## Horizontal rules

No.

[Exception](https://cirosantilli.com/markdown-style-guide/#end-of-a-header)

Use `---`

## Links

    [Text Bar](https://example.foo)

[Github](https://github.com)

Wrap automatic links in angle brackets `<>`: <https://github.com>