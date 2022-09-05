# 🧡 Stream

The `Stream` is the base class of all other streams.

### single()

Returns the produced value.

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('a static value');

console.log(stream.single());
// 'a static value'
```

### many()

Returns the produced array.

| Parameter | Type      | Default | Description   |
| --------- | --------- | ------- | ------------- |
| `length`  | `Integer` | `10`    | target length |

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('a static value');

console.log(stream.many(2));
// ['a static value', 'a static value']
```

### array()

Returns an [`ArrayStream`](array-stream.md) with the given length.

| Parameter | Type      | Default | Description                                             |
| --------- | --------- | ------- | ------------------------------------------------------- |
| `length`  | `Integer` | `10`    | target length of the [`ArrayStream`](array-stream.md)`` |

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .array(3)
  .map(i => i.toUpperCase());

console.log(stream.single());
// ['VALUE', 'VALUE', 'VALUE']
```

### format()

Returns a [`StringStream`](string-stream.md) that formats the produced input by using [@fluentfixture/format](../../fluentfixture-format/).

| Parameter  | Type     | Default | Description     |
| ---------- | -------- | ------- | --------------- |
| `template` | `String` |         | format template |

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .format('VALUE IS ${:upperCase()}');

console.log(stream.single());
// 'VALUE IS VALUE
```

### optional()

Returns a [`Stream`](stream.md) that may produce value or `undefined`.

| Parameter    | Type    | Default | Description                     |
| ------------ | ------- | ------- | ------------------------------- |
| `percentage` | `Float` | `0.5`   | chance causing it to be defined |

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .optional(0.3);

console.log(stream.single());
// undefined or 'value'
```

### nullable()

Returns a [`Stream`](stream.md) that may produce value or `null`.

| Parameter    | Type    | Default | Description                     |
| ------------ | ------- | ------- | ------------------------------- |
| `percentage` | `Float` | `0.5`   | chance causing it to be defined |

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .nullable(0.3);

console.log(stream.single());
// null or 'value'
```

### convert()

Returns a [`Stream`](stream.md) with maps the produced value to another type.

| Parameter | Type       | Default | Description        |
| --------- | ---------- | ------- | ------------------ |
| `fn`      | `Function` |         | converter function |

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .convert(i => i.length);

console.log(stream.single());
// 5
```

### apply()

Returns a [`Stream`](stream.md) with maps the produced value to the same type.

| Parameter | Type       | Default | Description    |
| --------- | ---------- | ------- | -------------- |
| `fn`      | `Function` |         | apply function |

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .apply(i => i.padStart(7, '*'));

console.log(stream.single());
// '**value'
```

### memo()

Memoizes and returns the same [`Stream`](stream.md) that always produces the same value.

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .apply(i => i.padStart(7, '*'))
  .memo();

console.log(stream.many(2));
// ['**value', '**value']
```

### dump()

Returns a [`Stream`](stream.md) with debugging points.

| Parameter | Type       | Default | Description        |
| --------- | ---------- | ------- | ------------------ |
| `fn`      | `Function` |         | debugging function |

```typescript
import { val } from '@fluentfixture/core';

// val() returns a Stream with a static value.
const stream = val('value')
  .dump(i => console.log(i))
  .apply(i => i.padStart(7, '*'));

console.log(stream.many(2));
// 'values'
// ['**value', '**value']
```
