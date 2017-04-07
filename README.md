# keyboardevent-key-polyfill

Polyfill for `KeyboardEvent.prototype.key`.

> **NOTE:** All major browsers [now support `KeyboardEvent.prototype.key`](http://caniuse.com/#feat=keyboardevent-key). Firefox already shipped with this for a while; recent versions of Edge, Chrome, and Safari also now have shipped support. This will still enable `KeyboardEvent.prototype.key` in environments where it may not yet be available.


## Example

__[View Demo](https://cvan.io/keyboardevent-key-polyfill/)__

<hr>

Say goodbye to this:

```js
document.addEventListener('keydown', function (e) {
  console.log('Code of key pressed:', e.which || e.keyCode);  // 39
});
```

And hello to this:

```js
document.addEventListener('keydown', function (e) {
  console.log('Name of key pressed:', e.key);  // ArrowRight
});
```

## Usage

### From standalone script

Just drop the script on your page and call the `polyfill` method.

```html
<script src="index.js"></script>
<script>keyboardeventKeyPolyfill.polyfill();</script>
```

If you're using AMD:

```js
require('keyboardevent-key-polyfill').polyfill();
```

### From npm (Node/Browserify/WebPack)

Install from [npm](https://www.npmjs.com/package/keyboardevent-key-polyfill):

```bash
npm install keyboardevent-key-polyfill
```

Then require the CommonJS module for use with [Browserify](http://browserify.org)/[webpack](https://webpack.js.org/):

```js
require('keyboardevent-key-polyfill').polyfill();
```


## License

All code and content within this source-code repository is licensed under the [**Creative Commons Zero v1.0 Universal** license (CC0 1.0 Universal; Public Domain Dedication)](LICENSE.md).

You can copy, modify, distribute and perform this work, even for commercial purposes, all without asking permission.

For more information, refer to these following links:

* a copy of the [license](LICENSE.md) in [this source-code repository](https://github.com/cvan/keyboardevent-key-polyfill)
* the [human-readable summary](https://creativecommons.org/publicdomain/zero/1.0/) of the [full text of the legal code](https://creativecommons.org/publicdomain/zero/1.0/legalcode)
* the [full text of the legal code](https://creativecommons.org/publicdomain/zero/1.0/legalcode)
