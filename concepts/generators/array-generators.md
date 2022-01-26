# Array Generators

This section covers array-related generator functions.

<table>
   <thead>
      <tr>
         <th>Name</th>
         <th>Returns</th>
         <th data-type="checkbox">Deterministic</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td><a href="array-generators.md#pick-array"><code>pick()</code></a></td>
         <td><a href="../streams/stream.md"><code>Stream</code></a></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="array-generators.md#take-array-count"><code>take()</code></a></td>
         <td><a href="../streams/array-stream.md"><code>ArrayStream</code></a></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="array-generators.md#shuffle-array"><code>shuffle()</code></a></td>
         <td><a href="../streams/array-stream.md"><code>ArrayStream</code></a></td>
         <td>false</td>
      </tr>
   </tbody>
</table>

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
