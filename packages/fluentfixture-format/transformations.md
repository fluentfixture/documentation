# Transformations

A transformation is a function that is chained in the format expression. Transformation functions are executed sequentially.

```typescript
"${path:func-1|func-2|func-3}"
```

In the expression above;

1. Execute `path`
2. Execute `func-1`
3. Execute `func-2`
4. Execute `func-3`

### Custom Transformations

[@fluentfixture/format](./) comes with lots of default transformation functions. In addition to these, custom providers can be defined.

```typescript
import { Formatter, Pipes } from '@fluentfixture/format';

const source = {
  balance: {
    amount: 12,
    currency: 'TRY'
  }
};

const pipes = Pipes.withDefaults()
  .register('inc', (val: number, arg: number) => val + arg)
  .register('amount', (val: any) => `[${val.amount} ${val.currency}]`);

const formatter = Formatter.create(pipes);

formatter.format('BALANCE=${balance:amount()}', source);
// BALANCE=[12 TRY]

formatter.format('NEXT AMOUNT=${balance.amount:inc(10)}', source);
// NEXT AMOUNT=22
```

### Default Transformations

#### String Utils

<table><thead><tr><th>Name</th><th data-type="select">Input Type</th><th data-type="select">Output Type</th><th>Docs</th></tr></thead><tbody><tr><td><code>lowerCase()</code></td><td></td><td></td><td><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">Mdn Docs</a></td></tr><tr><td><code>upperCase()</code></td><td></td><td></td><td><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">Mdn Docs</a></td></tr><tr><td><code>trim()</code></td><td></td><td></td><td><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">Mdn Docs</a></td></tr><tr><td><code>trimStart()</code></td><td></td><td></td><td><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">Mdn Docs</a></td></tr><tr><td><code>trimEnd()</code></td><td></td><td></td><td><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">Mdn Docs</a></td></tr><tr><td><code>padStart()</code></td><td></td><td></td><td><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">Mdn Docs</a></td></tr><tr><td><code>padEnd()</code></td><td></td><td></td><td><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">Mdn Docs</a></td></tr><tr><td><code>split()</code></td><td></td><td></td><td><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">Mdn Docs</a></td></tr><tr><td><code>camelCase()</code></td><td></td><td></td><td><a href="https://www.npmjs.com/package/change-case">Library Docs</a></td></tr><tr><td><code>constantCase()</code></td><td></td><td></td><td><a href="https://www.npmjs.com/package/change-case">Library Docs</a></td></tr><tr><td><code>dotCase()</code></td><td></td><td></td><td><a href="https://www.npmjs.com/package/change-case">Library Docs</a></td></tr><tr><td><code>headerCase()</code></td><td></td><td></td><td><a href="https://www.npmjs.com/package/change-case">Library Docs</a></td></tr><tr><td><code>paramCase()</code></td><td></td><td></td><td><a href="https://www.npmjs.com/package/change-case">Library Docs</a></td></tr><tr><td><code>pascalCase()</code></td><td></td><td></td><td><a href="https://www.npmjs.com/package/change-case">Library Docs</a></td></tr><tr><td><code>pathCase()</code></td><td></td><td></td><td><a href="https://www.npmjs.com/package/change-case">Library Docs</a></td></tr><tr><td><code>snakeCase()</code></td><td></td><td></td><td><a href="https://www.npmjs.com/package/change-case">Library Docs</a></td></tr><tr><td><code>capitalCase()</code></td><td></td><td></td><td><a href="https://www.npmjs.com/package/change-case">Library Docs</a></td></tr></tbody></table>

#### Array Utils

<table><thead><tr><th>Name</th><th data-type="select">Input Type</th><th data-type="select">Output Type</th><th>Docs</th></tr></thead><tbody><tr><td><code>join()</code></td><td></td><td></td><td><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">Mdn Docs</a></td></tr><tr><td><code>sort()</code></td><td></td><td></td><td><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">Mdn Docs</a></td></tr><tr><td><code>reverse()</code></td><td></td><td></td><td><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">Mdn Docs</a></td></tr></tbody></table>

#### Date Utils

<table><thead><tr><th>Name</th><th data-type="select">Input Type</th><th data-type="select">Output Type</th><th>Docs</th></tr></thead><tbody><tr><td><code>date("pattern")</code></td><td></td><td></td><td><a href="https://day.js.org/docs/en/display/format">Library Docs</a></td></tr></tbody></table>

#### Other Utils

<table><thead><tr><th>Name</th><th data-type="select">Input Type</th><th data-type="select">Output Type</th><th>Docs</th></tr></thead><tbody><tr><td><code>default(value)</code></td><td></td><td></td><td>Returns default</td></tr></tbody></table>
