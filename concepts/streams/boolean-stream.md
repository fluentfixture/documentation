# Boolean Stream

[`BooleanStream`](boolean-stream.md) extends the [`Stream`](stream.md)  class for boolean operations.

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
         <td><a href="boolean-stream.md#not"><code>not()</code></a></td>
         <td><a href="boolean-stream.md"><code>BooleanStream</code></a></td>
         <td>true</td>
      </tr>
   </tbody>
</table>

## not ()

Creates a [`BooleanStream`](boolean-stream.md) with [`Functional`](../factories/decorators/functional.md) decorator and the `not` operator.

```typescript
const stream = new BooleanStream(new ValueAdapter(true))
    .not();
    
console.log(stream.single());
// prints always false
```
