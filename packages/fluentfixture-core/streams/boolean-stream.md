# Boolean Stream

The `BooleanStream` is a [`Stream`](stream.md) that provides boolean-related methods.

### not()

Returns a [`BooleanStream`](boolean-stream.md) that changes the produced input.

```typescript
import { truthy } from '@fluentfixture/core';

const stream = truthy().not();

console.log(stream.many(5));
// [false, false, false, false, false]
```
