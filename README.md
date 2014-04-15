warpech-display-router
======================

A Custom Element to switch visible elements based on current window location

### Demo

[Click here to see a live demo](http://warpech.github.io/warpech-display-router)

### Usage

```html
<warpech-display-router>
  <warpech-display-route match-path="\/" display-selector="body pj-dashboard #container"></warpech-display-route>
  <warpech-display-route match-path="\/launcher\/workspace\/super-crm" display-selector="body pj-dashboard #workspaces .SuperCRM"></warpech-display-route>
</warpech-display-router>
```

Wrapper tags `<warpech-display-router>` are optional.

### Attributes

#### `match-path`

Specifies the regular expression that will be matched against current window URL path (`window.location.pathname` in JavaScript)

#### `display-selector`

Specifies the CSS selector that will be used to show/hide an element.

### How it works

- For each **warpech-display-route**, the window URL is checked against the regular expression provided in the `match-path` attribute.
- If there is a match, the query in `display-selector` is performed against DOM and the first found element is set with `display: block`. 
- If there is no match, the query in `display-selector` is performed against DOM and the first found element is set with `display: none`.

### License

MIT