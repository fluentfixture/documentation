# 💛 Number Stream

The `NumberStream` is a [`Stream`](stream.md) that provides number-related methods.

### add()

Returns an [`NumberStream`](number-stream.md)  that adds the given value to the produced output.

<table><thead><tr><th>Parameter</th><th data-type="select" data-multiple>Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><code>value</code></td><td></td><td></td><td>The value.</td></tr></tbody></table>

```typescript
import { num } from '@fluentfixture/core';

const stream = num(10).add(0.5);

console.log(stream.many(5));
// [10.5, 10.5, 10.5, 10.5, 10.5]
```

### multiply()

Returns an [`NumberStream`](number-stream.md)  that multiplies the given value with the produced output.

<table><thead><tr><th>Parameter</th><th data-type="select" data-multiple>Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><code>value</code></td><td></td><td></td><td>The value.</td></tr></tbody></table>

```typescript
import { num } from '@fluentfixture/core';

const stream = num(10).multiply(0.5);

console.log(stream.many(5));
// [5, 5, 5, 5, 5]
```

### subtract()

Returns an [`NumberStream`](number-stream.md)  that subtracts the given value from the produced output.

<table><thead><tr><th>Parameter</th><th data-type="select" data-multiple>Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><code>value</code></td><td></td><td></td><td>The value.</td></tr></tbody></table>

```typescript
import { num } from '@fluentfixture/core';

const stream = num(10).subtract(0.5);

console.log(stream.many(5));
// [9.5, 9.5, 9.5, 9.5, 9.5]
```

### divide()

Returns an [`NumberStream`](number-stream.md)  that divides the produced output to the given value.

<table><thead><tr><th>Parameter</th><th data-type="select" data-multiple>Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><code>value</code></td><td></td><td></td><td>The value.</td></tr></tbody></table>

```typescript
import { num } from '@fluentfixture/core';

const stream = num(10).divide(0.5);

console.log(stream.many(5));
// [20, 20, 20, 20, 20]
```

### mode()

Returns an [`NumberStream`](number-stream.md)  that calculates the mode of the produced value with the given value.

<table><thead><tr><th>Parameter</th><th data-type="select" data-multiple>Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><code>value</code></td><td></td><td></td><td>The value.</td></tr></tbody></table>

```typescript
import { num } from '@fluentfixture/core';

const stream = num(10).mode(3);

console.log(stream.many(5));
// [1, 1, 1, 1, 1]
```
