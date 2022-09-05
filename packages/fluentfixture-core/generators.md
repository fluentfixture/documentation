# 💎 Generators

In [@fluentfixture](../../), streams cannot be initialized directly. To take advantage of the stream's fluent interface, we can use generator functions.

### Booleans

#### bool()

Returns a [`BooleanStream`](streams/boolean-stream.md)  that produces a boolean value.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><code>percentage</code></td><td></td><td><code>0.5</code></td><td>Chance causing it to be <code>true</code>.</td></tr></tbody></table>

```typescript
import { bool } from '@fluentfixture/core';

const stream = bool(0.9);

console.log(stream.many(5));
// [true, true, false, true, true]
```

#### truthy()

Returns a [`BooleanStream`](streams/boolean-stream.md)  that always produces `true`.

```typescript
import { truthy } from '@fluentfixture/core';

const stream = truthy();

console.log(stream.many(5));
// [true, true, true, true, true]
```

#### falsy()

Returns a [`BooleanStream`](streams/boolean-stream.md)  that always produces `false`.

```typescript
import { falsy } from '@fluentfixture/core';

const stream = falsy();

console.log(stream.many(5));
// [false, false, false, false, false]
```

### Numbers

#### int()

Returns an [`NumberStream`](streams/number-stream.md)  that produces an integer value.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><code>min</code></td><td></td><td><code>0</code></td><td>Lower boundary.</td></tr><tr><td><code>max</code></td><td></td><td><code>1000</code></td><td>Upper boundary.</td></tr></tbody></table>

```typescript
import { int } from '@fluentfixture/core';

const stream = int(1, 10)

console.log(stream.many(5));
// [7, 1, 6, 4, 9]
```

#### real()

Returns an [`NumberStream`](streams/number-stream.md)  that produces a float value.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><code>min</code></td><td></td><td><code>0</code></td><td>Lower boundary.</td></tr><tr><td><code>max</code></td><td></td><td><code>1000</code></td><td>Upper boundary.</td></tr></tbody></table>

```typescript
import { real } from '@fluentfixture/core';

const stream = real(1, 10)

console.log(stream.many(5));
// [9.298, 3.86, 9.31, 8.38, 8.23]
```

#### num()

Returns an [`NumberStream`](streams/number-stream.md)  that always produces the given number.

<table><thead><tr><th>Parameter</th><th data-type="select" data-multiple>Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><code>value</code></td><td></td><td></td><td>The number.</td></tr></tbody></table>

```typescript
import { num } from '@fluentfixture/core';

const stream = num(1881);

console.log(stream.many(5));
// [1881, 1881, 1881, 1881, 1881]
```

#### zero()

Returns an [`NumberStream`](streams/number-stream.md)  that always produces `zero`.

```typescript
import { zero } from '@fluentfixture/core';

const stream = zero();

console.log(stream.many(5));
// [0, 0, 0, 0, 0]
```

#### one()

Returns an [`NumberStream`](streams/number-stream.md)  that always produces `one`.

```typescript
import { one } from '@fluentfixture/core';

const stream = one();

console.log(stream.many(5));
// [1, 1, 1, 1, 1]
```
