# Array Generators

This section covers array-related generator functions.

* [`pick()`](array-generators.md#pick-array)
* [`take()`](array-generators.md#take-array-count)
* [`shuffle()`](array-generators.md#shuffle-array)

## pick (array)

Creates a [`Stream`](../streams/stream.md) that picks an item from the given array.

| Name    | Description                                      |
| ------- | ------------------------------------------------ |
| `array` | An array that a random element will be selected. |

```typescript
import { pick } from '@fluentfixture/core';

const stream = pick(['1', '2', '3']);

console.log(stream.single()); 
// prints '1', '2' or '3'
```

## take (array, count)

Creates an [`ArrayStream`](../streams/array-stream.md) that selects random items from the given array with the given count.

| Name    | Description                                     |
| ------- | ----------------------------------------------- |
| `array` | An array that random elements will be selected. |
| `count` | The item count. The default value is `10`.      |

```typescript
import { pick } from '@fluentfixture/core';

const stream = take(['1', '2', '3'], 2);

console.log(stream.single()); 
// prints a subset of ['1', '2', '3'] with 2 items
```

## shuffle (array)

Creates an [`ArrayStream`](../streams/array-stream.md) that shuffles the given array.

| Name    | Description              |
| ------- | ------------------------ |
| `array` | An array to be shuffled. |

```typescript
import { shuffle } from '@fluentfixture/core';

const stream = shuffle(['1', '2', '3']);

console.log(stream.single()); 
// prints a suffled version of ['1', '2', '3']
```
