*This repository is a mirror of the [component](http://component.io) module [stagas/autocomplete](http://github.com/stagas/autocomplete). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/stagas-autocomplete`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# autocomplete

dropdown autocomplete for input elements

## Installing

```sh
$ component-install stagas/autocomplete
```

## API

Inherits all methods from [Dropdown](https://github.com/stagas/dropdown) and [Menu](https://github.com/stagas/menu).

### Autocomplete(input, [items], [asyncFn])

Attach autocomplete to an input element.

### Autocomplete.maxItems(n:Number)

Set the maximum number of visible items.

## Usage


With a default set:

```js
var autocomplete = require('autocomplete')
var ac = autocomplete(input, ["One", "Two", "Three"])
```

Using async results:

```js
autocomplete(input, function (str, callback) {
  someAsyncRequest(str, function (results) {
    callback(results)
  })
})
```

Both:

```js
autocomplete(input, ["One", "Two", "Three"], function (str, callback) {
  someAsyncRequest(str, function (results) {
    callback(results)
  })
})
```

## License

MIT
