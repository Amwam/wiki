# CSS Tricks

- [https://web.dev/one-line-layouts/](https://web.dev/one-line-layouts/)
- [CSS Tricks Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

## `place-items: center`

- [https://developer.mozilla.org/en-US/docs/Web/CSS/place-items](https://developer.mozilla.org/en-US/docs/Web/CSS/place-items)

First specify grid as the display method, and then write place-items: center on the same element. place-items is a shorthand to set both align-items and justify-items at once. By setting it to center, both align-items and justify-items are set to center.

```css
.parent {
  display: grid;
  place-items: center;
}
```
