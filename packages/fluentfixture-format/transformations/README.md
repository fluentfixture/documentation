# 🛠 Transformations

A transformation is a function that is chained in the format expression. Transformation functions are executed sequentially.

```typescript
"${path:func1()|func2()|func3()}"
```

In the expression above;

* execute `path`
* then execute `func1()`
* then execute `func2()`
* then execute `func3()`

### Naming Convention

A transformation's name must be a valid javascript function name. For clarity, the camel case naming convention is suggested.

### Parameters

A transformation function only accepts valid JSON values.

* `number`
* `string`
* `boolean`
* `null`
* `JSON object`
* `array`
