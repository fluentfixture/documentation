# Object Stream

[`ObjectStream`](object-stream.md) extends the [`Stream`](stream.md) class for object operations.

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
         <td><a href="object-stream.md#dynamic-property-factory"><code>dynamic()</code></a></td>
         <td><a href="object-stream.md"><code>ObjectStream</code></a></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="object-stream.md#static-property-value"><code>static()</code></a></td>
         <td><a href="object-stream.md"><code>ObjectStream</code></a></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="object-stream.md#lazy-property-fn"><code>lazy()</code></a></td>
         <td><a href="object-stream.md"><code>ObjectStream</code></a></td>
         <td>true</td>
      </tr>
   </tbody>
</table>

## dynamic (property, factory)

Creates an [`ObjectStream`](object-stream.md) with [`Property`](../factories/decorators/property.md) decorator, the given property and factory.

| Name       | Description                         |
| ---------- | ----------------------------------- |
| `property` | The property name.                  |
| `factory`  | The source factory of the property. |

```typescript
const obj = {
    key: 1
};

const stream = new ObjectStream(new ValueAdapter(obj))
    .dynamic('key', new ValueAdapter('value'));
    
console.log(stream.single());
// prints always object below
//  {
//    key: 'value'
//  }
```

## static (property, value)

Creates an [`ObjectStream`](object-stream.md) with [`Property`](../factories/decorators/property.md) decorator, the given property and value.

| Name       | Description                |
| ---------- | -------------------------- |
| `property` | The property name.         |
| `value`    | The value of the property. |

```typescript
const obj = {
    key: 1
};

const stream = new ObjectStream(new ValueAdapter(obj))
    .static('key', 'value');
    
console.log(stream.single());
// prints always object below
//  {
//    key: 'value'
//  }
```

## lazy (property, fn)

Creates an [`ObjectStream`](object-stream.md) with [`Lazy`](../factories/decorators/lazy.md) decorator, the given property and function.

| Name       | Description                          |
| ---------- | ------------------------------------ |
| `property` | The property name.                   |
| `fn`       | The source function of the property. |

```typescript
const obj = {
    key: 1
};

const stream = new ObjectStream(new ValueAdapter(obj))
    .lazy('keyAsString', (o) => o.key.toString());
    
console.log(stream.single());
// prints always object below
//  {
//    key: 1,
//    keyAsString: '1'
//  }
```
