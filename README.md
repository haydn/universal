# Universal

A CSS reset that strips away almost all of the default browser styles so you can
just set the values you want.

## Features

### Unsets browser defaults

The default styles are removed by a `all: unset` declaration applied to all
elements **except the following**:

- HTML `head` element
- HTML [metadata content](https://developer.mozilla.org/en-US/docs/Web/HTML/Content_categories#metadata_content) elements
- SVG elements
- MathML elements

### Uses box-sizing

All visible HTML elements are given a `box-sizing: border-box` declaration.

All `::before` and `::after` pseudo-elements are given a `box-sizing: inherit`
declaration.

### Retains block elements

Following elements are given a `display: block` declaration:

- `address`
- `article`
- `aside`
- `blockquote`
- `body`
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
- `li`
- `main`
- `nav`
- `ol`
- `p`
- `pre`
- `section`
- `ul`

### Retains tables layout

The `display` properties for table elements are reset back to their normal values:

- `table` (`display: table`)
- `thead` (`display: table-header-group`)
- `tbody` (`display: table-row-group`)
- `tfoot` (`display: table-footer-group`)
- `tr` (`display: table-row`)
- `th` (`display: table-cell`)
- `td` (`display: table-cell`)

### Give embedded content sensible defaults

All embedded content elements are given `display: block` and `max-width: 100%`
declarations:

- `audio`
- `canvas`
- `iframe`
- `img`
- `math`
- `object`
- `svg`
- `video`

## Accessibility

Because this reset removes all default browser styles, important defaults for
accessibility are removed. If you use this reset, you should add your own styles
to ensure your content accessible:

1. Links should have an underline or similar indicator identify them.
2. Elements should be highlighted when focused.
