<div align="center">
  <h1>
    <img src="logo.png" alt="Universal CSS reset" width="160" />
  </h1>
  <p>A CSS reset that reduces styles to the bare minimum.</p>
  <p>
    <img alt="npm" src="https://img.shields.io/npm/dw/@haydn/universal.svg">
  </p>
</div>

## Usage

You can add the CSS to a file directly via [unpkg](https://unpkg.com/):

```html
<link
  rel="stylesheet"
  href="https://unpkg.com/@haydn/universal@latest/universal.css"
/>
```

Alternatively, in a JavaScript project you can install the package via npm:

```sh
npm i @haydn/universal
```

If your project uses a bundler like Webpack or Parcel, you can import the CSS file directly:

```js
import "@haydn/universal/universal.css";
```

## Features

### Unset browser defaults

The default styles are removed by a `all: unset` declaration applied to **all
elements except the following**:

- HTML `head` element
- HTML [metadata content](https://developer.mozilla.org/en-US/docs/Web/HTML/Content_categories#metadata_content) elements
- HTML [embedded content](https://developer.mozilla.org/en-US/docs/Web/HTML/Content_categories#embedded_content) elements
- SVG elements
- MathML elements

### Use box-sizing

**All HTML elements** are given a `box-sizing: border-box` declaration **except** the
`head` element and [metadata
content](https://developer.mozilla.org/en-US/docs/Web/HTML/Content_categories#metadata_content)
elements.

All `::before` and `::after` pseudo-elements are given a `box-sizing: inherit`
declaration.

### Retain block elements

Following elements are given a `display: block` declaration:

- `address`
- `article`
- `aside`
- `audio`
- `blockquote`
- `body`
- `canvas`
- `dd`
- `details`
- `dialog`
- `div`
- `dl`
- `dt`
- `fieldset`
- `figcaption`
- `figure`
- `footer`
- `form`
- `h1`
- `h2`
- `h3`
- `h4`
- `h5`
- `h6`
- `header`
- `hgroup`
- `hr`
- `iframe`
- `img`
- `li`
- `main`
- `math`
- `nav`
- `object`
- `ol`
- `p`
- `pre`
- `section`
- `svg`
- `ul`
- `video`

### Retain tables layout

The `display` properties for table elements are reset back to their normal values:

- `table` (`display: table`)
- `thead` (`display: table-header-group`)
- `tbody` (`display: table-row-group`)
- `tfoot` (`display: table-footer-group`)
- `tr` (`display: table-row`)
- `th` (`display: table-cell`)
- `td` (`display: table-cell`)

Additionally, the `border-collapse` property is set to `collapse` for `table` elements.

### Sensible defaults for embedded content

All [embedded
content](https://developer.mozilla.org/en-US/docs/Web/HTML/Content_categories#embedded_content)
elements are given `border: none` and `max-width: 100%` declarations:

- `audio`
- `canvas`
- `iframe`
- `img`
- `math`
- `object`
- `svg`
- `video`

## Accessibility

This reset removes some important accessibility defaults. If you use this reset,
you should add your own styles to ensure your content is accessible, most
importantly:

1. Links should be identify with an underline or similar indicator.
2. Focusable elements should be highlighted when focused.
