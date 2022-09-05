# 💚 StringStream

The `StringStream` is a [`Stream`](stream.md) that provides string-related methods.

### trim()

Returns a [`StringStream`](string-stream.md) that trims the produced
output. [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

```typescript
import {text} from '@fluentfixture/core';

const stream = text(' text ').trim();

console.log(stream.single());
// 'text'
```

### trimStart()

Returns a [`StringStream`](string-stream.md) that trims (from start) the produced
output. [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

```typescript
import {text} from '@fluentfixture/core';

const stream = text(' text ').trimStart();

console.log(stream.single());
// 'text '
```

### trimEnd()

Returns a [`StringStream`](string-stream.md) that trims (from end) the produced
output. [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

```typescript
import {text} from '@fluentfixture/core';

const stream = text(' text ').trimEnd();

console.log(stream.single());
// ' text'
```

### padStart()

Returns a [`StringStream`](string-stream.md) that add pads (from start) to the produced
output. [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

<table>
    <thead>
    <tr>
        <th>Parameter</th>
        <th data-type="select" data-multiple>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td><code>length</code></td>
        <td>Integer</td>
        <td></td>
        <td>Target length</td>
    </tr>
    <tr>
        <td><code>char</code></td>
        <td>String</td>
        <td></td>
        <td>Pad character</td>
    </tr>
    </tbody>
</table>

```typescript
import {text} from '@fluentfixture/core';

const stream = text('text').padStart(7, '#');

console.log(stream.single());
// '###text'
```

### padEnd()

Returns a [`StringStream`](string-stream.md) that add pads (from end) to the produced
output. [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

<table>
    <thead>
    <tr>
        <th>Parameter</th>
        <th data-type="select" data-multiple>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td><code>length</code></td>
        <td>Integer</td>
        <td></td>
        <td>Target length</td>
    </tr>
    <tr>
        <td><code>char</code></td>
        <td>String</td>
        <td></td>
        <td>Pad character</td>
    </tr>
    </tbody>
</table>

```typescript
import {text} from '@fluentfixture/core';

const stream = text('text').padEnd(7, '#');

console.log(stream.single());
// 'text###'
```

### split()

Returns a [`ArrayStream`](array-stream.md) that splits the produced
output. [Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

<table>
    <thead>
    <tr>
        <th>Parameter</th>
        <th data-type="select" data-multiple>Type</th>
        <th>Default</th>
        <th>Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td><code>separator</code></td>
        <td>String, RegExp</td>
        <td></td>
        <td>Separator.</td>
    </tr>
    <tr>
        <td><code>limit</code></td>
        <td>Integer</td>
        <td>0</td>
        <td>Limit on the number of substrings to be included in the array.</td>
    </tr>
    </tbody>
</table>

```typescript
import { text } from '@fluentfixture/core';

const stream = text('1,2,3')
    .split(',')
    .map(i => `#${i}`)

console.log(stream.single());
// ['#1', '#2', '#3']
```
