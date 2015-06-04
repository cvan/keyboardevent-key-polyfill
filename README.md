# event-key-polyfill

Polyfill for `KeyboardEvent.prototype.key`.

Firefox has already shipped with this for a while, but this will normalise it for other browsers (e.g., Chrome).

<hr>

Say goodbye to this:

```js
document.body.addEventListener('keydown', function (e) {
  console.log('Code of key pressed:', e.which || e.keyCode);
});
```

And hello to this:

```js
document.body.addEventListener('keydown', function (e) {
  console.log('Name of key pressed:', e.key);
});
```
