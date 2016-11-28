# hapi-nunjucks-helpers
Helpers for hapi-nunjucks

### Usage

Use as you would a normal hapijs plugin.

### Options

 - `assets`
    - `dist` - Directories files are built to. Default: none.
    - `mappingFile` - File output by clientkit to map hashed assets.
    - `endpoint` - Base directory for assets. Default: none.
    - `cdn` - Optional domain for assets. Default: none.
    - `cache` - If `true`, caches contents of `mappingFile`. Default: `false`

### Filters:

**asset**

Reads from clientkit generated mapping file if available.

```html
<script src="{{ 'common.js' | asset }}"></script>
```

**cdn**

Prefixes asset with cdn path from `assets.cdn` property.

```html
<img src="{{ 'logos/logo.png' | cdn }}">
```

With css/js

```html
<script src="{{ 'common.js' | asset | cdn }}"></script>
```
