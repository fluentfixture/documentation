# Number Generators

This section covers number-related generator functions.

* ``[`real()`](number-generators.md#real-min-max)``
* ``[`int()`](number-generators.md#int-min-max)``
* ``[`num()`](number-generators.md#num-val)``
* ``[`one()`](number-generators.md#one)``
* ``[`zero()`](number-generators.md#zero)``

## real (min, max)

Creates a [`NumberStream`](../streams/number-stream.md) that generates a float number with the given boundaries.

| Name  | Description                                               |
| ----- | --------------------------------------------------------- |
| `min` | The minimum of the boundary. The default value is `0`.    |
| `max` | The maximum of the boundary. The default value is `1000`. |

```typescript
import { real } from '@fluentfixture/core';

console.log(real(1, 10).single()); 
// prints a float between 1 and 10
```

## int (min, max)

Creates a [`NumberStream`](../streams/number-stream.md) that generates an integer number with the given boundaries.

| Name  | Description                                               |
| ----- | --------------------------------------------------------- |
| `min` | The minimum of the boundary. The default value is `0`.    |
| `max` | The maximum of the boundary. The default value is `1000`. |

```typescript
import { int } from '@fluentfixture/core';

console.log(int(1, 10).single()); 
// prints an integer between 1 and 10
```

## num (val)

Creates a [`NumberStream`](../streams/number-stream.md) that generates always the given value.

| Name  | Description                 |
| ----- | --------------------------- |
| `val` | The number to be generated. |

```typescript
import { num } from '@fluentfixture/core';

console.log(num(10).single()); 
// prints always 10
```

## one ()

Creates a [`NumberStream`](../streams/number-stream.md) that generates always 1.

```typescript
import { one } from '@fluentfixture/core';

console.log(one().single()); 
// prints always 1
```

## zero ()

Ceates a [`NumberStream`](../streams/number-stream.md) that generates always 0.

```typescript
import { zero } from '@fluentfixture/core';

console.log(zero().single()); 
// prints always 0
```
