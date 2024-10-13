# Object Stream

The `ObjectStream` is a [`Stream`](stream.md) that provides object-related methods.

### static()

Returns an [`ObjectStream`](object-stream.md) that adds a property with the given value to the produced output.

| Parameter  | Type     | Default | Description    |
| ---------- | -------- | ------- | -------------- |
| `property` | `String` |         | property name  |
| `value`    | `Any`    |         | property value |

```typescript
import { int, obj, text } from '@fluentfixture/core';

const stream = obj({
    key: text('key'),
    value: int(1, 10)
});

const extendedStream = stream
    .static('id', 3);

console.log(extendedStream.single());
// {key: 'key', value: 10, id: 3}
```

### dynamic()

Returns an [`ObjectStream`](object-stream.md) that adds a property to the produced output with the given stream.

| Parameter  | Type     | Default | Description     |
| ---------- | -------- | ------- | --------------- |
| `property` | `String` |         | property name   |
| `stream`   | `Stream` |         | property source |

```typescript
import { int, obj, text } from '@fluentfixture/core';

const stream = obj({
    key: text('key'),
    value: int(1, 10)
});

const extendedStream = stream
    .dynamic('id', int(1, 100));

console.log(extendedStream.single());
// {key: 'key', value: 10, id: 28}
```

### lazy()

Returns an [`ObjectStream`](object-stream.md) that adds a property to the produced output by using the result of the given function.

| Parameter   | Type       | Default | Description        |
| ----------- | ---------- | ------- | ------------------ |
| `property`  | `String`   |         | property name      |
| `converter` | `Function` |         | converter function |

```typescript
import { int, obj, text } from '@fluentfixture/core';

const stream = obj({
    key: text('key'),
    value: int(1, 10)
});

const extendedStream = stream
    .lazy('id', (v) => v.key.toUpperCase());

console.log(extendedStream.single());
// {key: 'key', value: 4, id: 'KEY'}
```
