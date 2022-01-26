# Stream

[`Stream`](stream.md) is the superclass of all stream types.

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
         <td><a href="stream.md#single"><code>single()</code></a></td>
         <td><code>mock data</code></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="stream.md#convert-fn"><code>convert()</code></a></td>
         <td><a href="stream.md"><code>Stream</code></a> </td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="stream.md#apply-fn"><code>apply()</code></a></td>
         <td><code>concrete stream type</code></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="stream.md#optional-percentage"><code>optional()</code></a></td>
         <td><a href="stream.md"><code>Stream</code></a> </td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="stream.md#nullable-percentage"><code>nullable()</code></a></td>
         <td><a href="stream.md"><code>Stream</code></a> </td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="stream.md#array-length"><code>array()</code></a></td>
         <td><a href="array-stream.md"><code>ArrayStream</code></a></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="stream.md#format-template"><code>format()</code></a></td>
         <td><a href="string-stream.md"><code>StringStream</code></a></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="stream.md#memo"><code>memo()</code></a></td>
         <td><a href="stream.md"><code>Stream</code></a> </td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="stream.md#dump-fn"><code>dump()</code></a></td>
         <td><a href="stream.md"><code>Stream</code></a> </td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="stream.md#getfactory"><code>getFactory()</code></a></td>
         <td><code>decorated factory</code></td>
         <td>true</td>
      </tr>
   </tbody>
</table>

## single ()

Generates single data by using the decorated factory.

```typescript
const stream = new Stream(new IntegerFactory(1, 100)); // returns Stream<number>
    
console.log(stream.single());
// prints an integer between 1 and 100
```

## convert (fn)

Creates a [`Stream`](stream.md) with [`Functional`](../factories/decorators/functional.md) decorator and the given function. The underlying type of the new stream is the same as the return type of the given function.

| Name | Description             |
| ---- | ----------------------- |
| `fn` | The converter function. |

```typescript
const stream = new Stream(new IntegerFactory(1, 100)) // returns Stream<number>
    .convert((i) => i + 0.5)                          // returns Stream<number>
    .convert((i) => i.toString())                     // returns Stream<string>
    .convert((i) => i.length);                        // returns Stream<number>
    
console.log(stream.single());
// prints an integer between 3 and 5 (length of '1.5' and '100.5')
```

## apply (fn)

Creates a [`Stream`](stream.md) with [`Functional`](../factories/decorators/functional.md) decorator and the given function. The underlying type of the new stream is the same as the return type of the given function.

| Name | Description             |
| ---- | ----------------------- |
| `fn` | The converter function. |

```typescript
const stream = new NumberStream(new IntegerFactory(1, 100)) // returns NumberStream
    .apply((i) => i + 0.5)                                  // returns NumberStream
    .convert((i) => i + 0.5);                               // returns Stream<number>

console.log(stream.single());
// prints an integer between 2 and 101
```

## optional (percentage)

Creates a [`Stream`](stream.md) with [`Optional`](../factories/decorators/optional.md) decorator, which means it may generate a value or undefined.

| Name         | Description                                                                                     |
| ------------ | ----------------------------------------------------------------------------------------------- |
| `percentage` | A number within `[0, 1]` of how often the result should be defined. The default value is `0.5`. |

```typescript
const stream = new Stream(new IntegerFactory(1, 100)) // returns Stream<number>
    .convert((i) => i + 0.5)                          // returns Stream<number>
    .convert((i) => i.toString())                     // returns Stream<string>
    .optional();                                      // returns Stream<string | undefined>
    
console.log(stream.single());
// prints a string between '1.5' and '100.5' or undefined
```

## nullable (percentage)

Creates a [`Stream`](stream.md) with  [`Nullable`](../factories/decorators/nullable.md) decorator, which means it may generate a value or null.

| Name         | Description                                                                                     |
| ------------ | ----------------------------------------------------------------------------------------------- |
| `percentage` | A number within `[0, 1]` of how often the result should be defined. The default value is `0.5`. |

```typescript
const stream = new Stream(new IntegerFactory(1, 100)) // returns Stream<number>
    .convert((i) => i + 0.5)                          // returns Stream<number>
    .convert((i) => i.toString())                     // returns Stream<string>
    .nullable();                                      // returns Stream<string | null>
    
console.log(stream.single());
// prints a string between '1.5' and '100.5' or null
```

## array (length)

Creates an [`ArrayStream`](array-stream.md) with [`Iterator`](../factories/decorators/iterator.md) decorator and the given length.

| Name     | Description                                         |
| -------- | --------------------------------------------------- |
| `length` | The length of the array. The default value is `10`. |

```typescript
const stream = new Stream(new IntegerFactory(1, 100)) // returns Stream<number>
    .convert((i) => i + 0.5)                          // returns Stream<number>
    .convert((i) => i.toString())                     // returns Stream<string>
    .array(3);                                        // returns ArraySteream<string>
    
console.log(stream.single());
// prints an array that contains strings between '1.5' and '100.5' with 3 items.
```

## format (template)

Creates a [`StringStream`](string-stream.md) with [`Formatter`](../factories/decorators/formatter.md) decorator and the given template.

| Name       | Description              |
| ---------- | ------------------------ |
| `template` | The template expression. |

```typescript
const stream = new Stream(new IntegerFactory(1, 100)) // returns Stream<number>
    .convert((i) => i + 0.5)                          // returns Stream<number>
    .format('Number({})');                            // returns StringStream
    
console.log(stream.single());
// prints an a string between 'Number(1.5)' and 'Number(100.5)'
```

## memo ()

Creates a [`Stream`](stream.md) with [`Memo`](../factories/decorators/memo.md) decorator.

```typescript
const stream = new Stream(new IntegerFactory(1, 100)) // returns Stream<number>
    .convert((i) => i + 0.5)                          // returns Stream<number>
    .memo()                                           // returns Stream<number>
    .convert((i) => i.toString());                    // returns Stream<string>
    
console.log(stream.single());
// prints an a string between '1.5' and '100.5'

console.log(stream.single());
// prints the same output above
// the converter in '.convert((i) => i + 0.5)' executed only once
```

## dump (fn)

Creates a [`Stream`](stream.md) with [`Exporter`](../factories/decorators/exporter.md) decorator and the given function.

| Name | Description                            |
| ---- | -------------------------------------- |
| `fn` | The function that receives the result. |

```typescript
const stream = new Stream(new IntegerFactory(1, 100)) // returns Stream<number>
    .dump((i) => console.log(i))                      // returns Stream<number>
    .convert((i) => i + 0.5)                          // returns Stream<number>
    .dump((i) => console.log(i))                      // returns Stream<number>
    .convert((i) => i.toString());                    // returns Stream<string>
    
console.log(stream.single());
// prints;
// 1) An integer between 1 and 100
// 2) A number between 1.5 and 100.5
// 3) A string between '1.5' and '100.5'
```

## getFactory ()

Returns the decorated factory.

```typescript
const stream = new Stream(new IntegerFactory(1, 100)) // returns Stream<number>
    .convert((i) => i + 0.5);                         // returns Stream<number>
    
console.log(stream.single());
// prints a number between 1.5 and 100.5

const factory = stream.getFactory();

console.log(factory.single());
// prints a number between 1.5 and 100.5
```
