# Object Stream

``[`ObjectStream`](object-stream.md) extends the [`Stream`](stream.md) class for object operations.

* ``[`dynamic()`](object-stream.md#dynamic-property-factory)``
* ``[`static()`](object-stream.md#static-property-value)``
* ``[`lazy()`](object-stream.md#lazy-property-fn)``

## dynamic (property, factory)

Creates an [`ObjectStream`](object-stream.md) with a new or overwritten property with the given factory according to the given key.&#x20;

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

Creates an [`ObjectStream`](object-stream.md) with a new or overwritten property with the given value according to the given key.&#x20;

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

Creates an [`ObjectStream`](object-stream.md) with a new or overwritten property with a function that takes the previous state of the mock data according to the given key. It is handy for generating conditional mock data.

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
