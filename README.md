# fauxql
A SQL-based parser

## Installation

```
npm install --save fauxql
```

## Usage

```
var parser = require('fauxql');

console.log(JSON.stringify(parser.parse("hello='world' OR foo='bar'"), null, '  '));
```

### Output

```
{
  "conditions": [
    {
      "left": "hello",
      "op": "Equal",
      "right": "world"
    },
    {
      "joiner": "Or",
      "expression": {
        "left": "foo",
        "op": "Equal",
        "right": "bar"
      }
    }
  ]
}
```
