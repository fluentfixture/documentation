# Adapters

This section covers adapter-kind generator functions.

* [`nil()`](adapters.md#nil)
* [`undef()`](adapters.md#undef)
* [`val()`](adapters.md#val-value)
* [`from()`](adapters.md#from-fn)

## nil ()

Creates a [`Stream`](../streams/stream.md) that generates always null.

```typescript
import { nil } from '@fluentfixture/core';

console.log(nil().single()); 
// prints always null
```

## undef ()

Ceates a [`Stream`](../streams/stream.md) that generates always undefined.

```typescript
import { undef } from '@fluentfixture/core';

console.log(undef().single()); 
// prints always undefined
```

## val (value)

Creates a [`Stream`](../streams/stream.md) that generates always the given value.

| Name    | Description                                                  |
| ------- | ------------------------------------------------------------ |
| `value` | The value to be generated. The default value is `undefined`. |

```typescript
import { val } from '@fluentfixture/core';

console.log(val('str').single()); 
// prints always 'str'
```

## from (fn)

Creates a [`Stream`](../streams/stream.md) that generates always the result of the given function.

| Name | Description                                     |
| ---- | ----------------------------------------------- |
| `fn` | The function to be invoked for generating data. |

```typescript
import { from } from '@fluentfixture/core';

console.log(from(() => 'str').single()); 
// prints always 'str'
```
