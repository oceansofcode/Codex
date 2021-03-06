<!-- omit in toc -->
# CSS

<!-- omit in toc -->
## Index

- [Reset & Normalize](#reset--normalize)
- [Selectors](#selectors)
- [Font](#font)
- [Borders](#borders)
- [Lists](#lists)
- [Design Tips / Tricks](#design-tips--tricks)

---

## Reset & Normalize

> Normalize attempts to standardize css across all browsers while reset makes each look un-styled

---

## Selectors

- `li > a` - direct child
- `li + a` - next sibling
- `li ~ a` - general sibling
- `.class1.class2` - element with both classes
- `[src]` - elements with a `src` attribute
- `[input="checkbox"]` - elements with an attribute value
- `[input~="check"]` - elements with an attribute that contains the word
- `[input^="check"]` - elements with an attribute that begins with
- `[input$~"check"]` - elements with an attribute that ends with

---

## Font

- `text-transform` UPPER, lower, Capitalize
- `text-decoration` underline, overline, line-through, blink

<!-- omit in toc -->
### Leading

> term use for the vertical space between lines of text.

- `line`

<!-- omit in toc -->
### `@font-face`

- use a font even if it is not installed
- `src` path to the font
- `font-family` name of the font for the rest of the style sheet

---

## Borders

---

## Lists

---

## Design Tips / Tricks

- Light text on dark background, increase height between lines and weight of the font to make it easier to read
- For long spans of text reducing contrast helps readability
