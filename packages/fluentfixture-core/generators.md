# 💎 Generators

In [@fluentfixture](../../), streams cannot be initialized directly. To take advantage of the stream's fluent interface, we can use generator functions.

### Boolean

#### bool()

Returns a [`BooleanStream`](streams/boolean-stream.md)  that produces a boolean value.

| Parameter    | Type    | Default | Description                    |
| ------------ | ------- | ------- |--------------------------------|
| `percentage` | `Float` | `0.5`   | chance causing it to be `true` |

```typescript
import { bool } from '@fluentfixture/core';

const stream = bool(0.9);

console.log(stream.many(5));
// [true, true, false, true, true]
```

#### truthy()

Returns a [`BooleanStream`](streams/boolean-stream.md)  that always produces `true`.

```typescript
import { truthy } from '@fluentfixture/core';

const stream = truthy();

console.log(stream.many(5));
// [true, true, true, true, true]
```

#### falsy()

Returns a [`BooleanStream`](streams/boolean-stream.md)  that always produces `false`.

```typescript
import { falsy } from '@fluentfixture/core';

const stream = falsy();

console.log(stream.many(5));
// [false, false, false, false, false]
```

### Number

#### int()

Returns an [`NumberStream`](streams/number-stream.md)  that produces an integer value.

| Parameter | Type      | Default | Description    |
| --------- | --------- | ------- |----------------|
| `min`     | `Integer` | `0`     | lower boundary |
| `max`     | `Integer` | `1000`  | upper boundary |

```typescript
import { int } from '@fluentfixture/core';

const stream = int(1, 10)

console.log(stream.many(5));
// [7, 1, 6, 4, 9]
```

#### real()

Returns an [`NumberStream`](streams/number-stream.md)  that produces a float value.

| Parameter | Type    | Default | Description    |
| --------- | ------- | ------- |----------------|
| `min`     | `Float` | `0`     | lower boundary |
| `max`     | `Float` | `1000`  | upper boundary |

```typescript
import { real } from '@fluentfixture/core';

const stream = real(1, 10)

console.log(stream.many(5));
// [9.298, 3.86, 9.31, 8.38, 8.23]
```

#### num()

Returns an [`NumberStream`](streams/number-stream.md)  that always produces the given number.

| Parameter | Type     | Default | Description  |
| --------- | -------- | ------- |--------------|
| `value`   | `Number` |         | value        |

```typescript
import { num } from '@fluentfixture/core';

const stream = num(1881);

console.log(stream.many(5));
// [1881, 1881, 1881, 1881, 1881]
```

#### zero()

Returns an [`NumberStream`](streams/number-stream.md)  that always produces `zero`.

```typescript
import { zero } from '@fluentfixture/core';

const stream = zero();

console.log(stream.many(5));
// [0, 0, 0, 0, 0]
```

#### one()

Returns an [`NumberStream`](streams/number-stream.md)  that always produces `one`.

```typescript
import { one } from '@fluentfixture/core';

const stream = one();

console.log(stream.many(5));
// [1, 1, 1, 1, 1]
```

### String

#### text()

Returns a [`StringStream`](streams/string-stream.md) that always produces the given value.

| Parameter  | Type     | Default | Description  |
|------------|----------|---------|--------------|
| `str`      | `String` |         | string       |

```typescript
import { text } from '@fluentfixture/core';

const stream = text('hello');

console.log(stream.single());
// 'hello'
```

#### str()

Returns a [`StringStream`](streams/string-stream.md) that produces a string.

| Parameter   | Type       | Default | Description           |
|-------------|------------|---------|-----------------------|
| `charset`   | `String`   |         | included characters   |
| `length`    | `Integer`  | `10`    | target length         |

```typescript
import { str } from '@fluentfixture/core';

const stream = str('abc', 10);

console.log(stream.single());
// 'abcca'
```

#### hex()

Returns a [`StringStream`](streams/string-stream.md) that produces a hex string.

| Parameter   | Type       | Default | Description   |
|-------------|------------|---------|---------------|
| `length`    | `Integer`  | `10`    | target length |

```typescript
import { hex } from '@fluentfixture/core';

const stream = hex(10);

console.log(stream.single());
// '22c839cce0'
```

#### binary()

Returns a [`StringStream`](streams/string-stream.md) that produces a binary string.

| Parameter   | Type       | Default | Description   |
|-------------|------------|---------|---------------|
| `length`    | `Integer`  | `10`    | target length |

```typescript
import { binary } from '@fluentfixture/core';

const stream = binary(10);

console.log(stream.single());
// '1100001110'
```

#### octal()

Returns a [`StringStream`](streams/string-stream.md) that produces an octal string.

| Parameter   | Type       | Default | Description   |
|-------------|------------|---------|---------------|
| `length`    | `Integer`  | `10`    | target length |

```typescript
import { octal } from '@fluentfixture/core';

const stream = octal(10);

console.log(stream.single());
// '2025723760'
```

#### numeric()

Returns a [`StringStream`](streams/string-stream.md) that produces a numeric string.

| Parameter   | Type       | Default | Description   |
|-------------|------------|---------|---------------|
| `length`    | `Integer`  | `10`    | target length |

```typescript
import { numeric } from '@fluentfixture/core';

const stream = numeric(10);

console.log(stream.single());
// '0843683947'
```

#### alphabetic()

Returns a [`StringStream`](streams/string-stream.md) that produces an alphabetic string.

| Parameter   | Type       | Default | Description   |
|-------------|------------|---------|---------------|
| `length`    | `Integer`  | `10`    | target length |

```typescript
import { alphabetic } from '@fluentfixture/core';

const stream = alphabetic(10);

console.log(stream.single());
// 'KlmobUQbyt'
```

#### alphanumeric()

Returns a [`StringStream`](streams/string-stream.md) that produces an alphanumeric string.

| Parameter   | Type       | Default | Description   |
|-------------|------------|---------|---------------|
| `length`    | `Integer`  | `10`    | target length |

```typescript
import { alphanumeric } from '@fluentfixture/core';

const stream = alphanumeric(10);

console.log(stream.single());
// 'iZvY8UtXxh'
```

### Date

#### date()

Returns a [`DateStream`](streams/date-stream.md)  that produces a date.

| Parameter   | Type     | Default          | Description     |
|-------------|----------|------------------|-----------------|
| `min`       | `Date`   | `yesterday`      | lower boundary  |
| `max`       | `Date`   | `tomorrow`       | upper boundary  |

```typescript
import { date } from '@fluentfixture/core';

const stream = date();

console.log(stream.single());
// Tue Sep 06 2022 11:10:26 GMT+0300 (GMT+03:00)
```

#### now()

Returns a [`DateStream`](streams/date-stream.md) that produces the current date.

```typescript
import { now } from '@fluentfixture/core';

const stream = now();

console.log(stream.single());
// Tue Sep 06 2022 11:10:26 GMT+0300 (GMT+03:00)
```
