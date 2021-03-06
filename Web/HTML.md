<!-- omit in toc -->
# HTML

<!-- omit in toc -->
## Index

- [Semantics](#semantics)
- [Anchor Tag](#anchor-tag)
- [`<head>`](#head)
  - [`<meta>`](#meta)
  - [`<link>`](#link)
- [Images](#images)
  - [`<figure>`](#figure)
  - [`<map>`](#map)
  - [`<picture>`](#picture)
  - [SVG](#svg)
- [Tables](#tables)
- [Lists](#lists)
- [Iframe](#iframe)
- [Forms](#forms)
  - [Input](#input)
- [Tips and Tricks](#tips-and-tricks)

---

## Semantics

<!-- omit in toc -->
### Tags

- `<q>Hello World!</q>` - Single Line Quote
- `<blockquote cite="citation.com">My citation</blockquote>` - Paragraph block quote
- `<abbr title="HW">Hello World!</abbr>` - Abbreviation
- `<cite>Macbool</cite>` - Citation name
- `<dfn>Black Hole</dfn>` - Defining instance of a new term
- `<address>742 Evergreen Terrace</address>` - Block to contain address info (email + physical)
- `<del>` - Text that was deleted from a document (strikethrough)
- `<ins>` - Text that has been inserted into a document (italics)
- `<s>` - Strikethrough; no longer relevant but do not delete
- `title="test"` - Attribute to show a tooltip over an element
- `<bdo>` - Bi-Directional Override
- `<header>` - Defines a header for a document or a section
- `<nav>` - Defines a container for navigation links
- `<section>` - Defines a section in a document
- `<article>` - Defines an independent self-contained article
- `<aside>` - Defines content aside from the content
- `<footer>` - Defines a footer for a document or a section
- `<details>` - Defines additional details
- `<summary>` - Defines a heading for the `<details>` element
- `<code>`
- `<kbd>` - Represents user input, typically monospace
- `<samp>` - Program output
- `<pre>` - Preserve whitespace
- `<var>` - Define a variable in a programming context

<!-- omit in toc -->
### Best Practices

---

## Anchor Tag

1. `mailto:mail@example.com`
2. `target="_blank` → new tab
3. `#` Link to id inside page
4. `target="iframe_a"`

---

## `<head>`

### `<meta>`

> Hold info about the webpage in the `<head>`

- `http-equiv` binds the element to an HTTP Response header.

```html
<meta charset="UTF-8">
<meta name="description" content="Free Web tutorials">
<meta name="author" content="John Doe">
<meta name="keywords" content="HTML, CSS, XML, JavaScript">
<meta http-equiv="refresh" content="30">
<meta http-equiv="robots" content="nofollow / index, follow">
<meta http-equiv="pragma" content="no-cache"> <!-- Do not cache page -->
<meta http-equiv="expires" content="Fri, 04, Apr 2014 23:59:59 GMT"> <!-- Do not cache 
page -->
<meta http-equiv="Content-Security-Policy" content="default-src https">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

<!-- omit in toc -->
### `<base>`

> base url for all relative URLs in a page

### `<link>`

- `rel="home"`: references a home page or the top of some hierarchy.
- [Preload, Prefetch, Prebrowsing](https://css-tricks.com/prefetching-preloading-prebrowsing/)

---

## Images

### `<figure>`

> Hold image with a `<figcaption>` attribute

### `<map>`

> Different actions on parts of an image where you click. Different shapes and coordinates of area. Can also attach JS click events instead of a link.

``` html
<img src="workplace.jpg" alt="Workplace" usemap="#workmap">
<map name="workmap">
    <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">
    <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm">
    <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.htm">
</map>
```

### `<picture>`

> Flexibility when specifying image resources.

```html
<picture>
  <source media="(min-width: 650px)" srcset="img_food.jpg">
  <source media="(min-width: 465px)" srcset="img_car.jpg">
  <img src="img_girl.jpg">
</picture>
```

### SVG

---

## Tables

> `<tfoot>` and `<thead>` available for table

---

## Lists

> `<ol>` has different types corresponding to what kind of markers (letters, numbers, roman numerals)

---

## Iframe

> `<iframe>` displays a webpage inline a webpage

```html
<iframe src="demo_iframe.htm" name="iframe_a"></iframe>
<p><a href="https://www.w3schools.com" target="iframe_a">W3Schools.com</a></p>
```

---

## Forms

<!-- omit in toc -->
### Example

```html
<form action="/action_page.php" target="_blank" method="PUT" autocomplete="false" novalidate="true">
    <fieldset>
        <legend>Hello World</legend>
        <input type="radio"name="gender" value="male">
        <label for="male">Male</label><br>

        <select name="cars" size="3" multiple>
            <option value="saab">Saab</option>
            <option value="volvo">Volvo</option>
        </select>
    </fieldset>

    <input list="browsers">
    <datalist id="browsers">
        <option value="Internet Explorer">
        <option value="Firefox">
        <option value="Chrome">
        <option value="Opera">
        <option value="Safari">
    </datalist>
    <output for="a b"></output>
    <button type="submit">Click</button>
</form>
```

### Input

> Multitude of input types (color, datetime-local, file, month, range, reset, search, tel, time, url)

<!-- omit in toc -->
#### Attributes

- Checked
- disabled
- pattern (Regex)
- readonly
- size
- multiple (email + file)
- placeholder
- autofocus
- autocomplete

---

## Tips and Tricks

<!-- omit in toc -->
### Legacy Support

> `<!--[if lt IE 9]<script src="http://html5shim.googlecode.com/svn/trunk/html5.js"></script><![end if]>-->`
