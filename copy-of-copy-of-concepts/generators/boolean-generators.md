# Boolean Generators

This section covers boolean-related generator functions.

<table><thead><tr><th>Name</th><th>Returns</th><th data-type="checkbox">Deterministic</th></tr></thead><tbody><tr><td><a href="boolean-generators.md#bool-percentage"><code>pick()</code></a></td><td><a href="broken-reference"><code>BooleanStream</code></a></td><td>false</td></tr><tr><td><a href="boolean-generators.md#truthy"><code>truthy()</code></a></td><td><a href="broken-reference"><code>BooleanStream</code></a></td><td>true</td></tr><tr><td><a href="boolean-generators.md#falsy"><code>falsy()</code></a></td><td><a href="broken-reference"><code>BooleanStream</code></a></td><td>true</td></tr></tbody></table>

## bool (percentage)

Creates a [`BooleanStream`](broken-reference) that generates a boolean with the given percentage.

| Name          | Description                                                                                  |
| ------------- | -------------------------------------------------------------------------------------------- |
| `percentange` | A number within `[0, 1]` of how often the result should be true. The default value is `0.5`. |

```typescript
import { bool } from '@fluentfixture/core';

console.log(bool().single()); 
// prints true or false
```

## truthy ()

Creates a [`BooleanStream`](broken-reference) that generates always true.

```typescript
import { truthy } from '@fluentfixture/core';

console.log(truthy().single()); 
// prints always true
```

## falsy ()

Creates a [`BooleanStream`](broken-reference) that generates always false.

```typescript
import { falsy } from '@fluentfixture/core';

console.log(falsy().single()); 
// prints always false
```
