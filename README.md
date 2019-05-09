# mkdocs-add-teaser

An MkDocs plugin to add a CSS class to the first paragraph after the first heading 1 in all pages of your project.

This is useful if the first paragraph of your pages always contains information that should stand out from the rest of the text, e.g., that should be printed in bold.

The name of the CSS class can be customized.

## Installation

Install the package with pip:

```
pip install mkdocs-add-teaser
```

Enable the plugin in your mkdocs.yml:

```yaml
plugins:
    - search
    - mkdocs-add-teaser:
        teaser_class: "teaser"
```

> **Note:** If you have no `plugins` entry in your config file yet, you'll likely also want to add the `search` plugin. MkDocs enables it by default if there is no `plugins` entry set, but now you have to enable it explicitly.

Add the CSS class to your extra CSS file. Example:

```css
.teaser {
    font-weight: bold;
}
```

## Configuration


## Usage

### HTML before processing

This is the HTML that Markdown will produce:

```html
<h1 id="...">...</h1>
<p>First paragraph</p>
```

### HTML after processing

This is the HTML after this plugin has run:

```html
<h1 id="...">...</h1>
<p class="teaser">First paragraph</p>
```
