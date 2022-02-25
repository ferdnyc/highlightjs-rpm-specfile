`highlight.js` syntax definition for RPM spec files.

For more about highlight.js, see https://highlightjs.org/

For more about RPM, see https://rpm.org/

### Usage

Simply include the `highlight.js` script package in your webpage or node app, load up this module and apply it to `hljs`.

If you're not using a build system and just want to embed this in your webpage:

```html
<script src="/path/to/highlight.pack.js"></script>
<script src="/path/to/highlightjs-rpm-specfile/rpm-specfile.js"></script>
<script>
  hljs.registerLanguage('rpm-specfile', window.hljsDefineRpmSpecfile);
  hljs.highlightAll();
</script>
```

If you're using webpack / rollup / browserify / node:

```javascript
var hljs = require('highlightjs');
var hljsDefineRpmSpecfile = require('highlightjs-rpm-specfile');

hljsDefineRpmSpecfile(hljs);
hljs.highlightAll();
```

### Advanced

This is a pretty simple package, the only thing you might want to do differently is name the language something other than `rpm-specfile`. If you want to do this, simply `import { definer } from 'highlightjs-rpm-specfile';` and use it like: `hljs.registerLanguage('othername', definer);`.
