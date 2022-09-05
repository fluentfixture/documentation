# 💚 String Stream

The `StringStream` is a [`Stream`](stream.md) that provides string-related methods.

### trim()

Returns a [`StringStream`](string-stream.md) that trims the produced output. ([Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String))

```typescript
import {text} from '@fluentfixture/core';

const stream = text(' text ').trim();

console.log(stream.single());
// 'text'
```

### trimStart()

Returns a [`StringStream`](string-stream.md) that trims (from the start) the produced output. ([Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String))

```typescript
import {text} from '@fluentfixture/core';

const stream = text(' text ').trimStart();

console.log(stream.single());
// 'text '
```

### trimEnd()

Returns a [`StringStream`](string-stream.md) that trims (from the end) the produced output. ([Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String))

```typescript
import {text} from '@fluentfixture/core';

const stream = text(' text ').trimEnd();

console.log(stream.single());
// ' text'
```

### padStart()

Returns a [`StringStream`](string-stream.md) that add pads (from the start) to the produced output. ([Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String))

| Parameter | Type      | Default | Description   |
| --------- | --------- | ------- | ------------- |
| `length`  | `Integer` |         | target length |
| `char`    | `String`  | `' '`   | pad string    |

```typescript
import {text} from '@fluentfixture/core';

const stream = text('text').padStart(7, '#');

console.log(stream.single());
// '###text'
```

### padEnd()

Returns a [`StringStream`](string-stream.md) that add pads (from the end) to the produced output. ([Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String))

| Parameter | Type      | Default | Description   |
| --------- | --------- | ------- | ------------- |
| `length`  | `Integer` |         | target length |
| `char`    | `String`  | `' '`   | pad string    |

```typescript
import {text} from '@fluentfixture/core';

const stream = text('text').padEnd(7, '#');

console.log(stream.single());
// 'text###'
```

### split()

Returns an [`ArrayStream`](array-stream.md) that produces the split output. ([Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String))

| Parameter   | Type                 | Default | Description |
| ----------- | -------------------- | ------- | ----------- |
| `separator` | `String` or `RegExp` |         | separator   |
| `limit`     | `Integer`            | `0`     | split limit |

```typescript
import { text } from '@fluentfixture/core';

const stream = text('1,2,3')
    .split(',')
    .map(i => `#${i}`)

console.log(stream.single());
// ['#1', '#2', '#3']
```

### lowerCase()

Returns a [`StringStream`](string-stream.md) that converts the produced output to the lower case. ([Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String))

```typescript
import { text } from '@fluentfixture/core';

const stream = text('HELLO').lowerCase();

console.log(stream.single());
// 'hello'
```

### upperCase()

Returns a [`StringStream`](string-stream.md) that converts the produced output to the upper case. ([Mdn Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/String))

```typescript
import { text } from '@fluentfixture/core';

const stream = text('hello').upperCase();

console.log(stream.single());
// 'HELLO'
```

### camelCase()

Returns a [`StringStream`](string-stream.md) that converts the produced output to the camel case. ([Library Docs](https://www.npmjs.com/package/change-case))

```typescript
import { text } from '@fluentfixture/core';

const stream = text('hello world').camelCase();

console.log(stream.single());
// 'helloWorld'
```

### capitalCase()

Returns a [`StringStream`](string-stream.md) that converts the produced output to the capital case. ([Library Docs](https://www.npmjs.com/package/change-case))

```typescript
import { text } from '@fluentfixture/core';

const stream = text('hello world').capitalCase();

console.log(stream.single());
// 'Hello World'
```

### constantCase()

Returns a [`StringStream`](string-stream.md) that converts the produced output to the constant case. ([Library Docs](https://www.npmjs.com/package/change-case))

```typescript
import { text } from '@fluentfixture/core';

const stream = text('hello world').constantCase();

console.log(stream.single());
// 'HELLO_WORLD'
```

### pathCase()

Returns a [`StringStream`](string-stream.md) that converts the produced output to the path case. ([Library Docs](https://www.npmjs.com/package/change-case))

```typescript
import { text } from '@fluentfixture/core';

const stream = text('hello world').pathCase();

console.log(stream.single());
// 'hello/world'
```

### dotCase()

Returns a [`StringStream`](string-stream.md) that converts the produced output to the dot case. ([Library Docs](https://www.npmjs.com/package/change-case))

```typescript
import { text } from '@fluentfixture/core';

const stream = text('hello world').dotCase();

console.log(stream.single());
// 'hello.world'
```

### headerCase()

Returns a [`StringStream`](string-stream.md) that converts the produced output to the header case. ([Library Docs](https://www.npmjs.com/package/change-case))

```typescript
import { text } from '@fluentfixture/core';

const stream = text('hello world').headerCase();

console.log(stream.single());
// 'Hello-World'
```

### paramCase()

Returns a [`StringStream`](string-stream.md) that converts the produced output to the param case. ([Library Docs](https://www.npmjs.com/package/change-case))

```typescript
import { text } from '@fluentfixture/core';

const stream = text('hello world').paramCase();

console.log(stream.single());
// 'hello-world'
```

### pascalCase()

Returns a [`StringStream`](string-stream.md) that converts the produced output to the pascal case. ([Library Docs](https://www.npmjs.com/package/change-case))

```typescript
import { text } from '@fluentfixture/core';

const stream = text('hello world').pascalCase();

console.log(stream.single());
// 'HelloWorld'
```

### snakeCase()

Returns a [`StringStream`](string-stream.md) that converts the produced output to the snake case. ([Library Docs](https://www.npmjs.com/package/change-case))

```typescript
import { text } from '@fluentfixture/core';

const stream = text('hello world').snakeCase();

console.log(stream.single());
// 'hello_world'
```
