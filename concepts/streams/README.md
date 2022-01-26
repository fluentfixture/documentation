# Streams

> In software engineering, a fluent interface is an object-oriented API whose design relies extensively on method chaining. Its goal is to increase code legibility by creating a domain-specific language (DSL).  (↪[wiki](https://en.wikipedia.org/wiki/Fluent\_interface))

Stream is a factory wrapper (also factories) that provides a fluent interface by decorating factories. All methods of streams create other streams that wrap themselves. Like any factory, streams are also immutable and reusable types.

## Streams vs. factories

Streams are also a factory. Both of them are immutable and reusable types. Every structure designed with streams can also be created using factories. The only difference is that streams provide a fluent interface, but factories do not.

The following code snippets are equivalent. The first example uses streams, and the other one uses factories.

### Example by using streams

```typescript
const stream = new Stream(new IntegerFactory(1, 100))
    .convert((i) => i + 0.5)
    .convert((i) => i.toString());
    
console.log(stream.single()); 
// prints a string between '1.5' and '100.5'
```

### Example by using factories

```typescript
const factory = new IntegerFactory(1, 100);
const addHalf = new Functional(factory, (i) => i + 0.5);
const toString = new Functional(addHalf, (i) => i.toString());

console.log(toString.single()); 
// prints a string between '1.5' and '100.5'
```

## Stream types

Streams also provide data-type-specific operations. For this reason, FluentFixture provides seven stream types listed below.

| Name                                     | Type      |
| ---------------------------------------- | --------- |
| ``[`Stream`](stream.md)``                | `any`     |
| ``[`BooleanStream`](boolean-stream.md)`` | `boolean` |
| ``[`NumberStream`](number-stream.md)``   | `number`  |
| ``[`StringStream`](string-stream.md)``   | `string`  |
| ``[`DateStream`](date-stream.md)``       | `date`    |
| ``[`ObjectStream`](object-stream.md)``   | `object`  |
| ``[`ArrayStream`](array-stream.md)``     | `array`   |

## Conclusion

Streams provide a fluent interface, and there are many stream types according to underlying data type. In the following chapters, stream types are covered. After the stream types, short-hand stream builder functions called generators are introduced.
