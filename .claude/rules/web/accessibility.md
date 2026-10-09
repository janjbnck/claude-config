---
paths:
  - "**/*.tsx"
  - "**/*.jsx"
  - "**/*.svelte"
  - "**/*.html"
---

# Accessibility

## Headings and landmarks

- Every `section` and `nav` has a heading. If it shouldn't be visible, render it anyway with the `sr-only` class
- Heading levels follow the document outline: one `h1` per page, `h2` for sections, `h3` for items, `h4` below that. Change the look with styling, never by skipping levels

## Hidden and decorative content

- Decorative elements get `aria-hidden`: icons, blinking cursors, connector lines
- Icon-only links need an `sr-only` span with the label
- Animated or partial text renders the visible version with `aria-hidden` and the full text in an `sr-only` span

## Links

- External links open in a new tab with `target="_blank" rel="noopener noreferrer"`
- Text links to external sites end with an external link icon after the text, like `box-arrow-up-right` from Bootstrap Icons

## Semantics

- Use `<b>` for labels and visual highlighting, `<strong>` for important text

## Other

- Dates are wrapped in `<time>` with the ISO string in the `datetime` or `dateTime` attribute and the locale-formatted text inside
- Image `alt` texts are translated if the project uses i18n
