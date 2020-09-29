# Javascript

Javascript is a [programming language](programming-languages.md).

## Parsing JSON

The `JSON.parse()` method accepts a string and returns a Object based on the string passed.

```Javascript
const response = '{ "usename": "jake", "updated_at": "2020-08-31" }'
JSON.parse(response) // Object { usename: 'jake', updated_at: '2020-08-31' }
```

This method also accepts an optional reviver function can be provided to perform a transformation on the resulting object before it is returned.

```Javascript
const response = '{ "usename": "jake", "updated_at": "2020-08-31" }'
JSON.parse(response, (key, value) => {
   return key === updated_at ? Date(value) : value
}) // {usename: "jake", updated_at: "Mon Aug 31 2020 18:01:36 GMT-0300 (Brasilia Standard Time)"}
```

### Caveats

- JSON.parse() does not allow trailing commas

```Javascript
// both will throw a SyntaxError
JSON.parse('[1, 2, 3, 4, ]');
JSON.parse('{"foo" : 1, }');
```

- JSON.parse() does not allow single quotes

```Javascript
// will throw a SyntaxError
JSON.parse("{'foo': 1}");
```
