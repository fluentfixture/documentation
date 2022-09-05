# 💚 String Stream

The `StringStream` is a [`Stream`](stream.md) that provides string-related methods.

### trim()

Returns a [`StringStream`](string-stream.md) that trims the produced output. [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String)

```typescript
import {text} from '@fluentfixture/core';

const stream = text(' text ').trim();

console.log(stream.single());
// 'text'
```

### trimStart()

Returns a [`StringStream`](string-stream.md) that trims (from the start) the produced output. [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String)

```typescript
import {text} from '@fluentfixture/core';

const stream = text(' text ').trimStart();

console.log(stream.single());
// 'text '
```

### trimEnd()

Returns a [`StringStream`](string-stream.md) that trims (from the end) the produced output. [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String)

```typescript
import {text} from '@fluentfixture/core';

const stream = text(' text ').trimEnd();

console.log(stream.single());
// ' text'
```

### padStart()

Returns a [`StringStream`](string-stream.md) that add pads (from the start) to the produced output. [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String)

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><code>length</code></td><td></td><td></td><td>target length</td></tr><tr><td><code>char</code></td><td></td><td><code>' '</code></td><td>pad string</td></tr></tbody></table>

```typescript
import {text} from '@fluentfixture/core';

const stream = text('text').padStart(7, '#');

console.log(stream.single());
// '###text'
```

### padEnd()

Returns a [`StringStream`](string-stream.md) that add pads (from the end) to the produced output. [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String)

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><code>length</code></td><td></td><td></td><td>target length</td></tr><tr><td><code>char</code></td><td></td><td><code>' '</code></td><td>pad string</td></tr></tbody></table>

```typescript
import {text} from '@fluentfixture/core';

const stream = text('text').padEnd(7, '#');

console.log(stream.single());
// 'text###'
```

### split()

Returns an [`ArrayStream`](array-stream.md) that produces the split output. [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String)

<table><thead><tr><th>Parameter</th><th data-type="select" data-multiple>Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td><code>separator</code></td><td></td><td></td><td>separator</td></tr><tr><td><code>limit</code></td><td></td><td><code>0</code></td><td>split limit</td></tr></tbody></table>

```typescript
import { text } from '@fluentfixture/core';

const stream = text('1,2,3')
    .split(',')
    .map(i => `#${i}`)

console.log(stream.single());
// ['#1', '#2', '#3']
```
