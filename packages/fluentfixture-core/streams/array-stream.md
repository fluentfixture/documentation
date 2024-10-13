# Array Stream

The `ArrayStream` is a [`Stream`](stream.md) that provides array-related methods.

### pick()

Returns a [`Stream`](stream.md) that picks an item from the produced output.

```typescript
import { list } from '@fluentfixture/core';

const stream = list([1, 2, 3]).pick();

console.log(stream.single());
// 2
```

### join()

Returns a [`StringStream`](string-stream.md) that merges the produced output.

| Parameter   | Type     | Default | Description |
| ----------- | -------- | ------- | ----------- |
| `seperator` | `String` | `''`    | separator   |

```typescript
import { list } from '@fluentfixture/core';

const stream = list([1, 2, 3]).join('+');

console.log(stream.single());
// '1+2+3'
```

### sample()

Returns an [`ArrayStream`](array-stream.md) that samples the produced output.

| Parameter | Type      | Default | Description |
| --------- | --------- | ------- | ----------- |
| `size`    | `Integer` | `3`     | sample size |

```typescript
import { list } from '@fluentfixture/core';

const stream = list([1, 2, 3]).sample(2);

console.log(stream.single());
// [1, 2]
```

### sort()

Returns an [`ArrayStream`](array-stream.md) that sorts the produced output.

| Parameter | Type       | Default | Description   |
| --------- | ---------- | ------- | ------------- |
| `fn`      | `Function` |         | sort function |

```typescript
import { list } from '@fluentfixture/core';

const stream = list([3, 5, 4]).sort((a, b) => b - a);

console.log(stream.single());
// [5, 4, 3]
```

### map()

Returns an [`ArrayStream`](array-stream.md) that maps the produced output.

| Parameter | Type       | Default | Description  |
| --------- | ---------- | ------- | ------------ |
| `fn`      | `Function` |         | map function |

```typescript
import { list } from '@fluentfixture/core';

const stream = list([3, 5, 4]).map(i => i.toString());

console.log(stream.single());
// ['3', '4', '5']
```

### filter()

Returns an [`ArrayStream`](array-stream.md) that filters the produced output.

| Parameter | Type       | Default | Description     |
| --------- | ---------- | ------- | --------------- |
| `fn`      | `Function` |         | filter function |

```typescript
import { list } from '@fluentfixture/core';

const stream = list([3, 5, 4]).filter(i => i % 2 === 0);

console.log(stream.single());
// [4]
```
