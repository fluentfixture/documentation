# ⛓ Streams

> In software engineering, a fluent interface is an object-oriented API whose design relies extensively on method chaining. Its goal is to increase code legibility by creating a domain-specific language (DSL). (↪[wiki](https://en.wikipedia.org/wiki/Fluent\_interface))

In [@fluentfixture](../../../), factories are small and valuable units, but they are very incapable of building complex and conditional data. Streams are factory wrappers (stream is a kind of factory) that provide a fluent interface. All methods of streams create other streams that wrap themselves. Like any factory, streams are also immutable and reusable types.

{% hint style="info" %}
Stream instances cannot be initialized directly. Instead of this, [generator](../generators.md) functions can be used.
{% endhint %}

### Decomposition Of A Stream

In the following example, a stream is built by compositions of many components.&#x20;

```typescript
import { int } from '@fluentfixture/core';

const stream = int(1, 100)
  .add(0.5)
  .array(10)
  .sort((a,b) => a - b)
  .join('/')
  .format('numbers = ${}')
  .upperCase();

console.log(stream.single());
// Prints like;
// NUMBERS = 4.5/5.5/40.5/41.5/48.5/52.5/56.5/68.5/72.5/83.5
```

Let's decompose the stream above to understand the stream and factory concept.

| Code           | Output                                 | Sub-Component       | Job                                        |
| -------------- | -------------------------------------- | ------------------- | ------------------------------------------ |
| `int(1, 100)`  | ``[`NumberStream`](number-stream.md)`` | `IntegerFactory`    | generates an integer                       |
| `.add(0.5)`    | ``[`NumberStream`](number-stream.md)`` | `FunctionDecorator` | adds `0.5` to the previous output          |
| `.array(10)`   | ``[`ArrayStream`](array-stream.md)``   | `Iterator`          | Iterates to decorated factory              |
| `.sort(...)`   | ``[`ArrayStream`](array-stream.md)``   | `FunctionDecorator` | sorts the previous output                  |
| `.join(...)`   | ``[`StringStream`](string-stream.md)`` | `FunctionDecorator` | merge the previos output                   |
| `.format(...)` | ``[`StringStream`](string-stream.md)`` | `FormatDecorator`   | formats the previous output                |
| `.upperCase()` | ``[`StringStream`](string-stream.md)`` | `FunctionDecorator` | converts to upper case the previous outout |
