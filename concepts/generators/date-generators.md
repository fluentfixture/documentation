# Date Generators

This section covers date-related generator functions.

* [`date()`](date-generators.md#date-min-max)
* [`now()`](date-generators.md#now)
* [`yesterday()`](date-generators.md#yesterday)
* [`tomorrow()`](date-generators.md#yesterday-1)

## date (min, max)

Creates a [`DateStream`](../streams/date-stream.md) that generates a date with the given boundaries.

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
