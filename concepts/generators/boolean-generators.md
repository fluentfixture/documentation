# Boolean Generators

This section covers boolean-related generator functions.

* ``[`bool()`](boolean-generators.md#bool-percentage)``
* ``[`truthy()`](boolean-generators.md#truthy)``
* ``[`falsy()`](boolean-generators.md#falsy)``

## bool (percentage)

Creates a [`BooleanStream`](../streams/boolean-stream.md) that generates a boolean with the given percentage.

| Name          | Description                                                                                  |
| ------------- | -------------------------------------------------------------------------------------------- |
| `percentange` | A number within `[0, 1]` of how often the result should be true. The default value is `0.5`. |

```typescript
import { bool } from '@fluentfixture/core';

console.log(bool().single()); 
// prints true or false
```

## truthy ()

Creates a [`BooleanStream`](../streams/boolean-stream.md) that generates always true.

```typescript
import { truthy } from '@fluentfixture/core';

console.log(truthy().single()); 
// prints always true
```

## falsy ()

Creates a [`BooleanStream`](../streams/boolean-stream.md) that generates always false.

```typescript
import { falsy } from '@fluentfixture/core';

console.log(falsy().single()); 
// prints always false
```
