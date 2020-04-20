# Change SVG's path attribute with CSS.

It is possible to change a svg's path attribute with CSS (Chrome only?).

Here is an svg of a hambuger icons:

```html
<svg viewBox="0 0 32 32">
    <path d="M3,3 29,3 M3,16 29,16 M3,29 29,29"></path>
</svg>
```

The hamburger icon can be change to a X icon with CSS:

```css
svg {
    path {
        d: path("M3,3 29,29 M16,16 16,16 M3,29 29,3");
    }
}
```