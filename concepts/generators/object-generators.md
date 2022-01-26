# Object Generators

This section covers object-related generator functions.

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
         <td><a href="object-generators.md#obj-model"><code>pick()</code></a></td>
         <td><a href="../streams/object-stream.md"><code>ObjectStream</code></a></td>
         <td>true</td>
      </tr>
   </tbody>
</table>

## obj (model)

Creates an [`ObjectStream`](../streams/object-stream.md) that generates an object with the given model.

| Name    | Description                                                          |
| ------- | -------------------------------------------------------------------- |
| `model` | A key-value object model that all keys are an instance of a factory. |

```typescript
import { obj, bool, int, numeric } from '@fluentfixture/core';

const stream = obj({
    id: int(1, 100),
    isValid: bool(),
    code: numeric(4)
});

console.log(bool().single()); 
// prints an object that with model above
// for example:
//  {
//    id: 29,
//    isValid: true,
//    code: '1881'
//  }
```
