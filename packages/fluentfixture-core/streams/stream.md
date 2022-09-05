# Stream

The `Stream` is the base class of all streams.

### Instance Methods

#### single()

Returns the produced value.

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('a static value');

console.log(stream.single());
// 'a static value'
```

#### many()

Returns the produced array.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td>length</td><td></td><td><code>10</code></td><td>The length of the output.</td></tr></tbody></table>

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('a static value');

console.log(stream.many(2));
// ['a static value', 'a static value']
```

#### array()

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
