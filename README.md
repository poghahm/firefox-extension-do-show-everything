### `manifest.json`

The [manifest.json](manifest.json) file shows the excluded domains.

This should be done in a UI
to make it easier to add a site to the exclude list while browsing,
and so that an extension reload is not necessary.

### `css.css`

The [css.css](css.css) file has the meat of the extension,
which is this:

```css
*,
::before,
::after {
    animation: initial !important;
    clip-path: initial !important;
    contain: initial !important;
    filter: initial !important;
    flex-wrap: wrap !important;
    height: initial !important;
    max-height: initial !important;
    min-height: initial !important;
    opacity: initial !important;
    overflow: initial !important;
    position: initial !important;
    transform: initial !important;
    transition: initial !important;
    visibility: initial !important;
    z-index: initial !important;
}
```

The rest of the `css.css` file works with `js.js` to repeat the above, but harder.

### `js.js`

The [js.js](js.js) file visits all the html nodes looking for misbehavers
and adds classes and/or styles to discipline them.
