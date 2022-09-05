# 🖤 Date Stream

The `DateStream` is a [`Stream`](stream.md) that provides date-related methods.

### addMilliseconds()

Returns a [`DateStream`](date-stream.md) that adds milliseconds to the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().addMilliseconds(10);

console.log(stream.single());
// now + 10 milliseconds
```

### subtractMilliseconds()

Returns a [`DateStream`](date-stream.md) that subtracts milliseconds from the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().subtractMilliseconds(10);

console.log(stream.single());
// now - 10 milliseconds
```

### setMilliseconds()

Returns a [`DateStream`](date-stream.md) that sets the milliseconds of the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().setMilliseconds(10);

console.log(stream.single());
// now with milliseconds is 10
```

### getMilliseconds()

Returns a [`NumberStream`](number-stream.md) with the milliseconds parts of the produced output.

```typescript
import { now } from '@fluentfixture/core';

const stream = now().getMilliseconds();

console.log(stream.single());
// milliseconds part of the now
```

### addSeconds()

Returns a [`DateStream`](date-stream.md) that adds seconds to the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().addSeconds(10);

console.log(stream.single());
// now + 10 seconds
```

### subtractSeconds()

Returns a [`DateStream`](date-stream.md) that subtracts seconds from the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().subtractSeconds(10);

console.log(stream.single());
// now - 10 seconds
```

### setSeconds()

Returns a [`DateStream`](date-stream.md) that sets the seconds of the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().setSeconds(10);

console.log(stream.single());
// now with seconds is 10
```

### getSeconds()

Returns a [`NumberStream`](number-stream.md) with the seconds parts of the produced output.

```typescript
import { now } from '@fluentfixture/core';

const stream = now().getSeconds();

console.log(stream.single());
// seconds part of the now
```

### addHours()

Returns a [`DateStream`](date-stream.md) that adds hours to the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().addHours(10);

console.log(stream.single());
// now + 10 hours
```

### subtractHours()

Returns a [`DateStream`](date-stream.md) that subtracts hours from the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().subtractHours(10);

console.log(stream.single());
// now - 10 hours
```

### setHours()

Returns a [`DateStream`](date-stream.md) that sets the hours of the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().setHours(10);

console.log(stream.single());
// now with hours is 10
```

### getHours()

Returns a [`NumberStream`](number-stream.md) with the hours parts of the produced output.

```typescript
import { now } from '@fluentfixture/core';

const stream = now().getHours();

console.log(stream.single());
// hours part of the now
```


### addDays()

Returns a [`DateStream`](date-stream.md) that adds days to the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().addDays(10);

console.log(stream.single());
// now + 10 days
```

### subtractDays()

Returns a [`DateStream`](date-stream.md) that subtracts days from the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().subtractDays(10);

console.log(stream.single());
// now - 10 days
```

### setDaysOfMonth()

Returns a [`DateStream`](date-stream.md) that sets the days of month of the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().setDaysOfMonth(10);

console.log(stream.single());
// now with days of month is 10
```

### setDaysOfWeek()

Returns a [`DateStream`](date-stream.md) that sets the days of week of the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().setDaysOfWeek(2);

console.log(stream.single());
// now with days of week is 2
```

### getDaysOfMonth()

Returns a [`NumberStream`](number-stream.md) with the days of month parts of the produced output.

```typescript
import { now } from '@fluentfixture/core';

const stream = now().getDaysOfMonth();

console.log(stream.single());
// days of month part of the now
```

### getDaysOfWeek()

Returns a [`NumberStream`](number-stream.md) with the days of week parts of the produced output.

```typescript
import { now } from '@fluentfixture/core';

const stream = now().getDaysOfWeek();

console.log(stream.single());
// days of week part of the now
```

### addMonths()

Returns a [`DateStream`](date-stream.md) that adds months to the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().addMonths(10);

console.log(stream.single());
// now + 10 months
```

### subtractMonths()

Returns a [`DateStream`](date-stream.md) that subtracts months from the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().subtractMonths(10);

console.log(stream.single());
// now - 10 months
```

### setMonths()

Returns a [`DateStream`](date-stream.md) that sets the months of the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().setMonths(10);

console.log(stream.single());
// now with months is 10
```

### getMonths()

Returns a [`NumberStream`](number-stream.md) with the months parts of the produced output.

```typescript
import { now } from '@fluentfixture/core';

const stream = now().getMonths();

console.log(stream.single());
// months part of the now
```



### addYears()

Returns a [`DateStream`](date-stream.md) that adds years to the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().addYears(10);

console.log(stream.single());
// now + 10 years
```

### subtractYears()

Returns a [`DateStream`](date-stream.md) that subtracts years from the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().subtractYears(10);

console.log(stream.single());
// now - 10 years
```

### setYears()

Returns a [`DateStream`](date-stream.md) that sets the years of the produced output.

| Parameter  | Type      | Default | Description  |
|------------|-----------|---------|--------------|
| `value`    | `Integer` |         | value        |

```typescript
import { now } from '@fluentfixture/core';

const stream = now().setYears(10);

console.log(stream.single());
// now with years is 10
```

### getYears()

Returns a [`NumberStream`](number-stream.md) with the years parts of the produced output.

```typescript
import { now } from '@fluentfixture/core';

const stream = now().getYears();

console.log(stream.single());
// years part of the now
```


