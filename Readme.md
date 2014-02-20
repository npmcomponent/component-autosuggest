*This repository is a mirror of the [component](http://component.io) module [component/autosuggest](http://github.com/component/autosuggest). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-autosuggest`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# autosuggest

### Autosuggest values for text inputs

`<input type="text">` autosuggest component. [Try the demo][demo]!

Inspired from http://oak.cs.ucla.edu/cs144/projects/javascript/suggest1.html.

## Installation

```bash
$ component install component/autosuggest
```

## Example

```js
var autosuggest = require('autosuggest');
var input = document.querySelector('input[type="text"]');

// array of suggestions
var suggestions = [
  'Sunday',
  'Monday',
  'Tuesday',
  'Wednesday',
  'Thursday',
  'Friday',
  'Saturday'
];

// create an `autosuggest` instance
var suggest = autosuggest(input, suggestions);

// and you can change the array of suggestions to use if they get change
var newSuggestions = suggestions.concat([ 'Funday' ]);
suggest.set(newSuggestions);
```

## API

### autosuggest(el, [suggestions]) → Autosuggest

Returns an `Autosuggest` instance. The instance has `.start()` called on it if the
optional `suggestions` array is given, otherwise you must call `.set(array)` and
`.start()` manually.

### .set(array)

Sets a new array of Strings to use as the suggestions for the `Autosuggest`
instance.

#### .start()

Starts the autosuggesting for the `Autosuggest` instance.

#### .stop()

Stops the autosuggesting for the `Autosuggest` instance..

## License

  MIT

[demo]: http://component.github.com/autosuggest/
