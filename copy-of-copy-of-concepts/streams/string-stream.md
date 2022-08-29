# String Stream

[`StringStream`](broken-reference) extends the [`Stream`](broken-reference) class for string operations.

<table><thead><tr><th>Name</th><th>Returns</th><th data-type="checkbox">Deterministic</th></tr></thead><tbody><tr><td><a href="string-stream.md#trim"><code>trim()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#trimstart"><code>trimStart()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#trimend"><code>trimEnd()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#padstart-length-str"><code>padStart()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#padend-length-str"><code>padEnd()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#lowercase"><code>lowerCase()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#uppercase"><code>upperCase()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#camelcase"><code>camelCase()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#capitalcase"><code>capitalCase()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#constantcase"><code>constantCase()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#dotcase"><code>dotCase()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#headercase"><code>headerCase()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#paramcase"><code>paramCase()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#pascalcase"><code>pascalCase()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#snakecase"><code>snakeCase()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr><tr><td><a href="string-stream.md#pathcase"><code>pathCase()</code></a></td><td><a href="broken-reference"><code>StringStream</code></a></td><td>true</td></tr></tbody></table>

## trim ()

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `trim` operator.

```typescript
const stream = new StringStream(new ValueAdapter(' lorem ipsum '))
    .trim();
    
console.log(stream.single());
// prints always 'lorem ipsum'
```

## trimStart ()

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `trim-start` operator.

```typescript
const stream = new StringStream(new ValueAdapter(' lorem ipsum '))
    .trimStart();
    
console.log(stream.single());
// prints always 'lorem ipsum '
```

## trimEnd ()

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `trim-end` operator.

```typescript
const stream = new StringStream(new ValueAdapter(' lorem ipsum '))
    .trimEnd();
    
console.log(stream.single());
// prints always ' lorem ipsum'
```

## padStart (length, str)

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `pad-start` operator.

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

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `pad-end` operator.

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

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `lower-case` operator.

```typescript
const stream = new StringStream(new ValueAdapter('LOREM IPSUM'))
    .lowerCase();
    
console.log(stream.single());
// prints always 'lorem ipsum'
```

## upperCase ()

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `upper-case` operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .upperCase();
    
console.log(stream.single());
// prints always 'LOREM IPSUM'
```

## camelCase ()

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `camel-case` operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .camelCase();
    
console.log(stream.single());
// prints always 'loremIpsum'
```

## capitalCase ()

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `capital-case` operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .capitalCase();
    
console.log(stream.single());
// prints always 'Lorem Ipsum'
```

## constantCase ()

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the c`onstant-case` operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .constantCase();
    
console.log(stream.single());
// prints always 'LOREM_IPSUM'
```

## dotCase ()

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `dot-case` operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .dotCase();
    
console.log(stream.single());
// prints always 'lorem.ipsum'
```

## headerCase ()

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `header-case` operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .headerCase();
    
console.log(stream.single());
// prints always 'Lorem-Ipsum'
```

## paramCase ()

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `param-case` operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .paramCase();
    
console.log(stream.single());
// prints always 'lorem-ipsum'
```

## pascalCase ()

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `pascal-case` operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .pascalCase();
    
console.log(stream.single());
// prints always 'LoremIpsum'
```

## snakeCase ()

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `snake-case` operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .snakeCase();
    
console.log(stream.single());
// prints always 'lorem_ipsum'
```

## pathCase ()

Creates a [`StringStream`](broken-reference) with [`Functional`](broken-reference) decorator and the `path-case` operator.

```typescript
const stream = new StringStream(new ValueAdapter('lorem ipsum'))
    .pathCase();
    
console.log(stream.single());
// prints always 'lorem/ipsum'
```
