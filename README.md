# keyboardevent-key-polyfill

Polyfill for `KeyboardEvent.prototype.key`.

Firefox has already shipped with this for a while, but this will normalise it for other browsers (e.g., Chrome).


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

Then require the CommonJS module for use with Browserify/WebPack:

```js
require('keyboardevent-key-polyfill').polyfill();
```

## License

[MIT](LICENCSE)
