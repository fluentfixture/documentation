# Date Generators

This section covers date-related generator functions.

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
         <td><a href="date-generators.md#date-min-max"><code>date()</code></a></td>
         <td><a href="../streams/date-stream.md"><code>DateStream</code></a></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="date-generators.md#now"><code>now()</code></a></td>
         <td><a href="../streams/date-stream.md"><code>DateStream</code></a></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="date-generators.md#yesterday"><code>yesterday()</code></a></td>
         <td><a href="../streams/date-stream.md"><code>DateStream</code></a></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="date-generators.md#tomorrow"><code>tomorrow()</code></a></td>
         <td><a href="../streams/date-stream.md"><code>DateStream</code></a></td>
         <td>false</td>
      </tr>
   </tbody>
</table>

## date (min, max)

Creates a [`DateStream`](../streams/date-stream.md) that generates a date within the given boundary.

| Name  | Description                                                             |
| ----- | ----------------------------------------------------------------------- |
| `min` | The minimum of the boundary. The default value is the date of now.      |
| `max` | The minimum of the boundary. The default value is the date of tomorrow. |

```typescript
import { date } from '@fluentfixture/core';

console.log(date().single()); 
// prints a date between now and tomorrow
```

## now ()

Creates a [`DateStream`](../streams/date-stream.md) that generates a date that is the date of now.

```typescript
import { now } from '@fluentfixture/core';

console.log(now().single()); 
// prints the date of the no
```

## yesterday ()

Creates a [`DateStream`](../streams/date-stream.md) that generates a date that is the date of yesterday.

```typescript
import { yesterday } from '@fluentfixture/core';

console.log(yesterday().single()); 
// prints the date of the yesterday
```

## tomorrow ()

Creates a [`DateStream`](../streams/date-stream.md) that generates a date that is the date of tomorrow.

```typescript
import { tomorrow } from '@fluentfixture/core';

console.log(tomorrow().single()); 
// prints the date of the tomorrow
```
