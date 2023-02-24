# Built-In Pipes

### String Pipes

| Name                | Input Type | Output Type | Docs                                                                                                 |
| ------------------- | ---------- | ----------- | ---------------------------------------------------------------------------------------------------- |
| `lowerCase()`       | `String`   | `String`    | [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String) |
| `upperCase()`       | `String`   | `String`    | [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String) |
| `trim()`            | `String`   | `String`    | [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String) |
| `trimStart()`       | `String`   | `String`    | [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String) |
| `trimEnd()`         | `String`   | `String`    | [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String) |
| `padStart(len, ch)` | `String`   | `String`    | [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String) |
| `padEnd(len, ch)`   | `String`   | `String`    | [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String) |
| `split(ch)`         | `String`   | `Array`     | [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String) |
| `camelCase()`       | `String`   | `String`    | [Library Docs](https://www.npmjs.com/package/change-case)                                            |
| `constantCase()`    | `String`   | `String`    | [Library Docs](https://www.npmjs.com/package/change-case)                                            |
| `dotCase()`         | `String`   | `String`    | [Library Docs](https://www.npmjs.com/package/change-case)                                            |
| `headerCase()`      | `String`   | `String`    | [Library Docs](https://www.npmjs.com/package/change-case)                                            |
| `paramCase()`       | `String`   | `String`    | [Library Docs](https://www.npmjs.com/package/change-case)                                            |
| `pascalCase()`      | `String`   | `String`    | [Library Docs](https://www.npmjs.com/package/change-case)                                            |
| `pathCase()`        | `String`   | `String`    | [Library Docs](https://www.npmjs.com/package/change-case)                                            |
| `snakeCase()`       | `String`   | `String`    | [Library Docs](https://www.npmjs.com/package/change-case)                                            |
| `capitalCase()`     | `String`   | `String`    | [Library Docs](https://www.npmjs.com/package/change-case)                                            |

### Array Pipes

| Name        | Input Type | Output Type | Docs                                                                                                |
| ----------- | ---------- | ----------- | --------------------------------------------------------------------------------------------------- |
| `join(ch)`  | `Array`    | `String`    | [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array) |
| `sort()`    | `Array`    | `Array`     | [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array) |
| `reverse()` | `Array`    | `Array`     | [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array) |

### Date Pipes

| Name              | Input Type | Output Type | Docs                                                      |
| ----------------- | ---------- | ----------- | --------------------------------------------------------- |
| `date("pattern")` | `Date`     | `String`    | [Library Docs](https://day.js.org/docs/en/display/format) |

### Other Pipes

| Name             | Input Type | Output Type | Docs            |
| ---------------- | ---------- | ----------- | --------------- |
| `default(value)` | `Any`      | `Any`       | Returns default |
