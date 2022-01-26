# Number Generators

This section covers number-related generator functions.

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
         <td><a href="number-generators.md#real-min-max"><code>real()</code></a></td>
         <td><a href="../streams/number-stream.md"><code>NumberStream</code></a></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="number-generators.md#int-min-max"><code>int()</code></a></td>
         <td><a href="../streams/number-stream.md"><code>NumberStream</code></a></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="number-generators.md#num-val"><code>num()</code></a></td>
         <td><a href="../streams/number-stream.md"><code>NumberStream</code></a></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="number-generators.md#one"><code>one()</code></a></td>
         <td><a href="../streams/number-stream.md"><code>NumberStream</code></a></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="number-generators.md#zero"><code>zero()</code></a></td>
         <td><a href="../streams/number-stream.md"><code>NumberStream</code></a></td>
         <td>true</td>
      </tr>
   </tbody>
</table>

## real (min, max)

Creates a [`NumberStream`](../streams/number-stream.md) that generates a float number within the given boundary.

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

Creates a [`NumberStream`](../streams/number-stream.md) that generates an integer number within the given boundary.

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
