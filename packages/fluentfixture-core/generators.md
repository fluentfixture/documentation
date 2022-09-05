# 💎 Generators

In [@fluentfixture](../../), streams cannot be initialized directly. To take advantage of the stream's fluent interface, we can use generator functions.

### Booleans

#### bool()

Returns a [`BooleanStream`](streams/booleanstream.md)  that produces a boolean value.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td>percentage</td><td></td><td><code>0.5</code></td><td>Chance causing it to be <code>true</code>.</td></tr></tbody></table>

```typescript
import { bool } from '@fluentfixture/core';

const stream = bool(0.9);

console.log(stream.many(5));
// [true, true, false, true, true]
```

#### truthy()

Returns a [`BooleanStream`](streams/booleanstream.md)  that always produces `true`.

```typescript
import { truthy } from '@fluentfixture/core';

const stream = truthy();

console.log(stream.many(5));
// [true, true, true, true, true]
```

#### falsy()

Returns a [`BooleanStream`](streams/booleanstream.md)  that always produces `false`.

```typescript
import { falsy } from '@fluentfixture/core';

const stream = falsy();

console.log(stream.many(5));
// [false, false, false, false, false]
```
