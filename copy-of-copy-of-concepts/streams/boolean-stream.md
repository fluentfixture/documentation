# Boolean Stream

[`BooleanStream`](broken-reference) extends the [`Stream`](broken-reference) class for boolean operations.

<table><thead><tr><th>Name</th><th>Returns</th><th data-type="checkbox">Deterministic</th></tr></thead><tbody><tr><td><a href="boolean-stream.md#not"><code>not()</code></a></td><td><a href="broken-reference"><code>BooleanStream</code></a></td><td>true</td></tr></tbody></table>

## not ()

Creates a [`BooleanStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `not` operator.

```typescript
const stream = new BooleanStream(new ValueAdapter(true))
    .not();
    
console.log(stream.single());
// prints always false
```
