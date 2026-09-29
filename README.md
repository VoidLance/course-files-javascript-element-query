# JavaScript Element Query

A small, dependency-free browser demo and utility library for finding and manipulating DOM elements with CSS selectors. The page includes an interactive demo, and `index.js` provides reusable helpers for common DOM operations.

## Why use it?

- Query one element or a collection of elements using standard CSS selectors.
- Create, append, remove, clone, replace, wrap, and unwrap elements.
- Read and update text, HTML, attributes, classes, and inline styles.
- Work with focus, scrolling, visibility, position, and dimensions.
- Explore basic selector-based operations from the page's interactive demo.

## Get started

No package manager, build step, or external dependency is required.

1. Clone or download this repository.
2. Open `index.html` in a modern web browser.
3. In the demo, enter a CSS selector (the default is `header`) and choose an action.

To use the helpers in another page, include the script and call its functions after the script has loaded:

```html
<script src="index.js"></script>
<script>
  const heading = queryElement('h1');
  if (heading) {
    setElementText('h1', 'Updated heading');
    addElementClass('h1', 'highlight');
  }
</script>
```

The script is a classic browser script, not an ES module. Its functions are available in the page's global scope. Examples of other helpers include `queryAllElements(selector)`, `createElement(tagName, options)`, `setElementAttribute(selector, attribute, value)`, `removeElement(selector)`, and `getElementText(selector)`. Selectors use the browser's standard CSS selector syntax; missing matches generally return `null` (or an empty array for `queryAllElements`) and may produce a console warning.

## Project files

- `index.html` — the interactive demo page and its styles.
- `index.js` — selector, DOM manipulation, and demo interaction functions.

## Get help

For questions, bug reports, or feature requests, [open an issue](https://github.com/VoidLance/course-files-javascript-element-query/issues).

## Maintainers and contributing

This project is maintained by its repository contributors. Contributions are welcome: open an issue to discuss a change, or submit a pull request with a focused improvement and a description of how you tested it. Since the project has no build or test setup, verify changes in a browser by opening `index.html`.
