# Number Stream

[`NumberSteam`](number-stream.md) extends the [`Stream`](stream.md) class for numeric operations.

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
         <td><a href="number-stream.md#add-num"><code>add()</code></a></td>
         <td><a href="number-stream.md"><code>NumberSteam</code></a></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="number-stream.md#subtract-num"><code>subtract()</code></a></td>
         <td><a href="number-stream.md"><code>NumberSteam</code></a></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="number-stream.md#multiply-num"><code>multiply()</code></a></td>
         <td><a href="number-stream.md"><code>NumberSteam</code></a></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="number-stream.md#divide-num"><code>divide()</code></a></td>
         <td><a href="number-stream.md"><code>NumberSteam</code></a></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="number-stream.md#mode-num"><code>mode()</code></a></td>
         <td><a href="number-stream.md"><code>NumberSteam</code></a></td>
         <td>true</td>
      </tr>
   </tbody>
</table>

## add (num)

Creates a [`NumberStream`](number-stream.md) with [`Functional`](../factories/decorators/functional.md) decorator and the `add` operator.

| Name  | Description             |
| ----- | ----------------------- |
| `num` | The number to be added. |

```typescript
const stream = new NumberStream(new ValueAdapter(10))
    .add(10);
    
console.log(stream.single());
// prints always 20
```

## subtract (num)

Creates a [`NumberStream`](number-stream.md) with [`Functional`](../factories/decorators/functional.md) decorator and the `subtract` operator.

| Name  | Description                  |
| ----- | ---------------------------- |
| `num` | The number to be subtracted. |

```typescript
const stream = new NumberStream(new ValueAdapter(10))
    .subtract(10);
    
console.log(stream.single());
// prints always 0
```

## multiply (num)

Creates a [`NumberStream`](number-stream.md) with [`Functional`](../factories/decorators/functional.md) decorator and the `multiply` operator.

| Name  | Description                  |
| ----- | ---------------------------- |
| `num` | The number to be multiplied. |

```typescript
const stream = new NumberStream(new ValueAdapter(10))
    .multiply(10);
    
console.log(stream.single());
// prints always 100
```

## divide (num)

Creates a [`NumberStream`](number-stream.md) with [`Functional`](../factories/decorators/functional.md) decorator and the `divide` operator.

| Name  | Description               |
| ----- | ------------------------- |
| `num` | The number to be divisor. |

```typescript
const stream = new NumberStream(new ValueAdapter(10))
    .divide(10);
    
console.log(stream.single());
// prints always 1
```

## mode (num)

Creates a [`NumberStream`](number-stream.md) with [`Functional`](../factories/decorators/functional.md) decorator and the `mode` operator.

| Name  | Description               |
| ----- | ------------------------- |
| `num` | The number to be divisor. |

```typescript
const stream = new NumberStream(new ValueAdapter(10))
    .mode(10);
    
console.log(stream.single());
// prints always 0
```
