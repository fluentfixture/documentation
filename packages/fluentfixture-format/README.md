# @fluentfixture/format

### Introduction

The **@fluentfixture/format** is a flexible string format library that provides formatting functionality with an extensible transformation capabilities.

### Installation

```bash
$ npm install @fluentfixture/format
```

### Usage

The [@fluentfixture/format](./) utilities can be used with global `format` and `compile` methods or a new `Formatter` instance. The following code snippet shows an example usage of global `compile` method.

{% hint style="info" %}
The more example can be found on [how-to-use.md](how-to-use.md "mention")section.
{% endhint %}

```typescript
import { compile } from '@fluentfixture/format';

const template = compile('${name:capitalCase()}, ${age:default("N/A")} >> ${colors:join("+")}');

template.format({
  name: 'john',
  age: 32,
  colors: ['red', 'black']
});
// "John, 32 >> red+black"

template.format({
  name: 'john',
  surname: 'doe'
});
// "John, N/A >> "  

template.format({
  name: 'john',
  admin: false,
  age: 11,
  colors: ['blue']
});
// "John, 11 >> blue"
```
