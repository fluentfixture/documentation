# Stream

The `Stream` is the base class of all other streams.

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

### convert()

Returns a [`Stream`](stream.md) with maps the produced value to another type.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td>fn</td><td></td><td></td><td>The converter function.</td></tr></tbody></table>

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .convert(i => i.length);

console.log(stream.single());
// 5
```

### apply()

Returns a [`Stream`](stream.md) with maps the produced value to the same type.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td>fn</td><td></td><td></td><td>The apply function.</td></tr></tbody></table>

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .apply(i => i.padStart(7, '*'));

console.log(stream.single());
// '**value'
```

### memo()

Memoize and returns the same [`Stream`](stream.md) that produces always the same value.

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .apply(i => i.padStart(7, '*'))
  .memo();

console.log(stream.many(2));
// ['**value', '**value']
```

### dump()

Returns a [`Stream`](stream.md) with debugging points.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td>fn</td><td></td><td></td><td>The debugging function.</td></tr></tbody></table>

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .dump(i => console.log(i))
  .apply(i => i.padStart(7, '*'));

console.log(stream.many(2));
// 'values'
// ['**value', '**value']
```
