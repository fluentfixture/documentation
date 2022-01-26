# Array Stream

{% hint style="info" %}
The following code snippets contain constructors of the internal classes. In FluentFixture, there is no way to initialize these classes directly, but these code snippets help understand the core concepts of the library. These classes can be initialized by using factory methods, [generators](../generators/).
{% endhint %}

``[`ArrayStream`](array-stream.md) extends the [`Stream`](stream.md) class for array operations.

* ``[`pick()`](array-stream.md#pick)``
* ``[`sample()`](array-stream.md#sample-size)``
* ``[`shuffle()`](array-stream.md#shuffle)``
* ``[`map()`](array-stream.md#map-fn)``
* ``[`filter()`](array-stream.md#filter-fn)``
* ``[`sort()`](array-stream.md#sort-fn)``

## pick ()

Creates a [`Stream`](stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the pick operator.

```typescript
const stream = new ArrayStream(new ValueAdapter([1, 2, 3]))
    .pick();
    
console.log(stream.single());
// prints 1, 2 or 3
```

## sample (size)

Creates an [`ArrayStream`](array-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the sample operator. The result is the subset of the initial array.

| Name   | Description                           |
| ------ | ------------------------------------- |
| `size` | The sample size. The default is `10`. |

```typescript
const stream = new ArrayStream(new ValueAdapter([1, 2, 3]))
    .sample(2);
    
console.log(stream.single());
// prints an array that subset of [1, 2, 3] with two items
```

## shuffle ()

Creates an [`ArrayStream`](array-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the shuffle operator. The result array contains the same elements with the initial array but different order.

```typescript
const stream = new ArrayStream(new ValueAdapter([1, 2, 3]))
    .shuffle(2);
    
console.log(stream.single());
// prints an array that contains [1, 2, 3] with random order
```

## map (fn)

Creates an [`ArrayStream`](array-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the map operator. This method works the same as how [Array#map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/map) works. The underlying type of the new stream is the same as the return type of the given map function.

| Name | Description       |
| ---- | ----------------- |
| `fn` | The map function. |

```typescript
const stream = new ArrayStream(new ValueAdapter([1, 2, 3]))
    .map((i) => i.toString());
    
console.log(stream.single());
// prints ['1', '2', '3']
```

## filter (fn)

Creates an [`ArrayStream`](array-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the filter operator. This method works the same as how [Array#filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/filter) works. The underlying type of the new stream is the same as the initial stream.

| Name | Description          |
| ---- | -------------------- |
| `fn` | The filter function. |

```typescript
const stream = new ArrayStream(new ValueAdapter([1, 2, 3]))
    .filter((i) => i % 2 === 0);
    
console.log(stream.single());
// prints [2]
```

## sort (fn)

Creates an [`ArrayStream`](array-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the sort operator. This method works the same as how [Array#sort()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/sort) works. The underlying type of the new stream is the same as the initial stream.

| Name | Description                                                            |
| ---- | ---------------------------------------------------------------------- |
| `fn` | The sort function. The default value is the default sorting algorithm. |

```typescript
const stream = new ArrayStream(new ValueAdapter([1, 2, 3]))
    .sort((l,r) => r-l);
    
console.log(stream.single());
// prints [3, 2, 1]
```
