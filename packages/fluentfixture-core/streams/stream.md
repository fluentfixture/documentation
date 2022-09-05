# Stream

The `Stream` is the base class of all streams.

### single()

Returns the produced value.

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('a static value');

console.log(stream.single());
// 'a static value'
```

### many()

Returns the produced array.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td>length</td><td></td><td><code>10</code></td><td>The length of the output.</td></tr></tbody></table>

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('a static value');

console.log(stream.many(2));
// ['a static value', 'a static value']
```

### array()

Returns an [`ArrayStream`](arraystream.md) with the given length.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td>length</td><td></td><td><code>10</code></td><td>The length of the new <code>ArrayStream</code>.</td></tr></tbody></table>

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .array(3)
  .map(i => i.toUpperCase());

console.log(stream.single());
// ['VALUE', 'VALUE', 'VALUE']
```

### format()

Returns a [`StringStream`](stringstream.md) that formats the produced input by using [@fluentfixture/format](../../fluentfixture-format/).

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td>template</td><td></td><td></td><td>Format template.</td></tr></tbody></table>

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .format('VALUE IS ${:upperCase()}');

console.log(stream.single());
// 'VALUE IS VALUE
```

### optional()

Returns a [`Stream`](stream.md) that may produce value or `undefined`.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td>percentage</td><td></td><td><code>0.5</code></td><td>Chance causing it to be defined.</td></tr></tbody></table>

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .optional(0.3);

console.log(stream.single());
// undefined or 'value'
```

### nullable()

Returns a [`Stream`](stream.md) that may produce value or `null`.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td>percentage</td><td></td><td><code>0.5</code></td><td>Chance causing it to be defined.</td></tr></tbody></table>

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .nullable(0.3);

console.log(stream.single());
// null or 'value'
```
