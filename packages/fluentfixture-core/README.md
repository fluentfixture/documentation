# @fluentfixture/core

### Introduction

The **@fluentfixture/core** provides various data generators for different use cases.
All generators offer a fluent interface for manipulating data, including sorting, creating conditional values, and more.

### Installation

```bash
$ npm install @fluentfixture/core
```

{% hint style="info" %}
The internals of the package and other utilities can be found on [streams](streams/ "mention") and [generators.md](generators.md "mention") sections.
{% endhint %}

### Example

Let us consider the following requirements. We need;
- One hundred products that are ordered by their prices,
- Each product has a price that ends with .95,
- Each product has a code field with the "id-color" format calculated using generated values,
- Each product has the same parent category with random id and name but the same type.
- Half of them have stock.

```typescript
import { alphabetic, bool, hex, int, obj, pick } from '@fluentfixture/core';

// Defines a price generator with amount and the currency fields.
const price = obj({
    amount: int(100, 1000).add(0.95),
    currency: pick(['USD', 'EUR', 'GBP', 'TRY']),
});

// Defines a color generator. (hex + pad + uppercase)
const color = hex(6).padStart(7, '#').upperCase();

// Defines a category with constant id.
const category = obj({
    id: int(1, 100),
    name: alphabetic().headerCase(),
    type: alphabetic(4, 8).memo()
})

// Defines a product generator.
const product = obj({
    id: int(1, 999),
    name: alphabetic(10, 20).capitalCase(),
    category: category,
    description: alphabetic(20, 40).optional(),
    hasStock: bool(0.5),
    color: color,
    price: price,
});

// 1) Adds 'code' field using generated values.
// 2) Iterates the model.
// 3) Sorts the generated models by their prices.
const products = product
    .lazy('code', (p) => `${p.id}-${p.color}`)
    .array(10)
    .sort((a, b) => a.price.amount - b.price.amount);

// Print all products
console.log(products.single());

// Print details of the first product.
console.log(product.format('[${id}] ${name:titleCase()} => ${price.amount}'));
```
