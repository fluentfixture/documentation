# String Stream

{% hint style="info" %}
The following code snippets contain constructors of the internal classes. In FluentFixture, there is no way to initialize these classes directly, but these code snippets help understand the core concepts of the library. These classes can be initialized by using factory methods, [generators](../generators/).
{% endhint %}

``[`StringStream`](string-stream.md) extends the [`Stream`](stream.md) class for string operations.

* ``[`trim()`](string-stream.md#trim)``
* ``[`trimStart()`](string-stream.md#trimstart)``
* ``[`trimEnd()`](string-stream.md#trimend)``
* ``[`padStart()`](string-stream.md#padstart-length-str)``
* ``[`padEnd()`](string-stream.md#padend-length-str)``
* ``[`lowerCase()`](string-stream.md#lowercase)``
* ``[`upperCase()`](string-stream.md#uppercase)``
* ``[`camelCase()`](string-stream.md#camelcase)``
* ``[`capitalCase()`](string-stream.md#capitalcase)``
* ``[`constantCase()`](string-stream.md#constantcase)``
* ``[`dotCase()`](string-stream.md#dotcase)``
* ``[`headerCase()`](string-stream.md#headercase)``
* ``[`paramCase()`](string-stream.md#paramcase)``
* ``[`pascalCase()`](string-stream.md#pascalcase)``
* ``[`snakeCase()`](string-stream.md#snakecase)``
* ``[`pathCase()`](string-stream.md#pathcase)``

## trim ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the trim operator.

```typescript
const stream = new StringStream(new ValueAdapter(' lorem ipsum '))
    .trim();
    
console.log(stream.single());
// prints always 'lorem ipsum'
```

## trimStart ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the trim-start operator.

```typescript
const stream = new StringStream(new ValueAdapter(' lorem ipsum '))
    .trimStart();
    
console.log(stream.single());
// prints always 'lorem ipsum '
```

## trimEnd ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the trim-end operator.

```typescript
const stream = new StringStream(new ValueAdapter(' lorem ipsum '))
    .trimEnd();
    
console.log(stream.single());
// prints always ' lorem ipsum'
```

## padStart (length, str)

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the pad-start operator.

| Name     | Description                             |
| -------- | --------------------------------------- |
| `length` | The target length of the string.        |
| `str`    | The pad string. The default is `space`. |

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .padStart(15, '*');
    
console.log(stream.single());
// prints always '****lorem ipsum'
```

## padEnd (length, str)

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the pad-end operator.

| Name     | Description                             |
| -------- | --------------------------------------- |
| `length` | The target length of the string.        |
| `str`    | The pad string. The default is `space`. |

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .padEnd(15, '*');
    
console.log(stream.single());
// prints always 'lorem ipsum****'
```

## lowerCase ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the lower-case operator.

```typescript
const stream = new StringStream(new ValueAdapter('LOREM IPSUM'))
    .lowerCase();
    
console.log(stream.single());
// prints always 'lorem ipsum'
```

## upperCase ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the upper-case operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .upperCase();
    
console.log(stream.single());
// prints always 'LOREM IPSUM'
```

## camelCase ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the camel-case operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .camelCase();
    
console.log(stream.single());
// prints always 'loremIpsum'
```

## capitalCase ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the capital-case operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .capitalCase();
    
console.log(stream.single());
// prints always 'Lorem Ipsum'
```

## constantCase ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the constant-case operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .constantCase();
    
console.log(stream.single());
// prints always 'LOREM_IPSUM'
```

## dotCase ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the dot-case operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .dotCase();
    
console.log(stream.single());
// prints always 'lorem.ipsum'
```

## headerCase ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the header-case operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .headerCase();
    
console.log(stream.single());
// prints always 'Lorem-Ipsum'
```

## paramCase ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the param-case operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .paramCase();
    
console.log(stream.single());
// prints always 'lorem-ipsum'
```

## pascalCase ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the pascal-case operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .pascalCase();
    
console.log(stream.single());
// prints always 'LoremIpsum'
```

## snakeCase ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the snake-case operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .snakeCase();
    
console.log(stream.single());
// prints always 'lorem_ipsum'
```

## pathCase ()

Creates a [`StringStream`](string-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the path-case operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .pathCase();
    
console.log(stream.single());
// prints always 'lorem/ipsum'
```
