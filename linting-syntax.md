# Markdown Linting Syntax Guide

The intention of this document is to provide clarity and standardize internal
documentation written in Markdown.

## Goal

Create a testable Markdown standard, balancing readability and ease of maintenance.
Establish ruleset for codebase Markdown linting.

Inspired by and primarily derived from the rational and references of
[Ciro Santilli](https://cirosantilli.com/markdown-style-guide)

## The Basics

- Asterisk format for **bold**: `**bold**`
- Underscore format for _italics_: `_italics_`
- Or when you **_really_ mean** it.

**Lint Parameters**: `"MD049": { "style": "underscore" }`,
                     `"MD050": { "style": "asterisk" }`

### Whitespace

- Force linebreaks with empty line. No trailing whitespace.
- No consecutive blank lines outside of code blocks.

**Lint Parameter**: `"whitespace": true`

### Line Length

Line length maintains the widely adopted 80 character standard. As near as
anyone can tell this is to maintain backwards compatibility.

![backward compatibility](https://upload.wikimedia.org/wikipedia/commons/thumb/5/58/FortranCardPROJ039.agr.jpg/320px-FortranCardPROJ039.agr.jpg "Compatible!")

We exempt the content of code blocks from this restriction.

**Lint Parameter**: `"MD013": { "code_blocks": false }`

## Headings

- Header text should be in `atx` style with no closing `#`, a single space separating
  `#` from text, and surrounded by newlines (excepting document start which
  should always be an `h1`).
  
  ```markdown
  # Header 1

  ## Header 2

  ### Header 3
  ```

**Lint Parameter**: `"MD003": { "style": atx }`

## Lists

### Unordered Lists

Denoted with `-.` (period added to illustrate space) and surrounded by newlines
with nested lists and paragraphs indenting 2 spaces above the parent.

```markdown
Is that a monkey?

- Orangutan
  - Ape
  - Librarian
  - Language

      Orangutans speak Orangutan.
      Humans only listen in bewilderment.

  - Ook
- Millennium
  - Hand
    - Shrimp

Buggerit
```

**Lint Parameter**: `"MD004": { "style": dash }`

### Ordered List

Markdown automatically renumbers ordered lists on render. With this in place,
lazy numbering should be preferred, especially for long, nested lists.

```markdown
1. Foo
1. Bar
   1. Foofoo
   1. Barbar
1. Baz
```

1. Foo
1. Bar
   1. Foofoo
   1. Barbar
1. Baz

Special attention should be paid to nested code block indentation to avoid
"breaking" a list.

```markdown
1. A thing

    ```language
    code related to thing
    ```

2. Another thing
```

## Code

### Inline Code

- Single backticks without surrounding whitespace.

```markdown
# Bad
` .this-is-not-good `

# Good
`.this-is-better`
```

### Fenced code blocks

- Blocks align with the current indent level
- Preceded with a newline and 3 backticks
- Language explicitly defined ` ```language `
- Closed with 3 backticks and a newline.

## Horizontal rules

_Don't_ use horizontal rules (see [rationale](https://cirosantilli.com/markdown-style-guide/#horizontal-rules))
except to delineate the [end of a header](https://cirosantilli.com/markdown-style-guide/#end-of-a-header)
not followed by a new header.

Use three hyphens without spaces `---`:

```markdown
# Header

Content

~~~

Outside header.
```

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
