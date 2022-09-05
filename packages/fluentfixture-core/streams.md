# ⛓ Streams

> In software engineering, a fluent interface is an object-oriented API whose design relies extensively on method chaining. Its goal is to increase code legibility by creating a domain-specific language (DSL). (↪[wiki](https://en.wikipedia.org/wiki/Fluent\_interface))

In [@fluentfixture](../../), factories are small and valuable units, but they are very incapable of building complex and conditional data. Streams are factory wrappers (stream is a kind of factory) that provide a fluent interface. All methods of streams create other streams that wrap themselves. Like any factory, streams are also immutable and reusable types.

{% hint style="info" %}
Stream instances cannot be initialized directly. Instead of this, [generator](generators.md) functions can be used.
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

<table><thead><tr><th>Code</th><th data-type="select">Output</th><th data-type="select">Sub-Component</th><th>Job</th></tr></thead><tbody><tr><td><code>int(1, 100)</code></td><td></td><td></td><td>generates an integer.</td></tr><tr><td><code>.add(0.5)</code></td><td></td><td></td><td>adds <code>0.5</code> to the previous output.</td></tr><tr><td><code>.array(10)</code></td><td></td><td></td><td>Iterates to decorated factory.</td></tr><tr><td><code>.sort(...)</code></td><td></td><td></td><td>sorts the previous output.</td></tr><tr><td><code>.join(...)</code></td><td></td><td></td><td>merge the previos output.</td></tr><tr><td><code>.format(...)</code></td><td></td><td></td><td>formats the previous output.</td></tr><tr><td><code>.upperCase()</code></td><td></td><td></td><td>converts to upper case the previous outout.</td></tr></tbody></table>
