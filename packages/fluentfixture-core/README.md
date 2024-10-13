# @fluentfixture/core

### Introduction

The **@fluentfixture/core** package offers various data generators for various use cases. Each of them supports a fluent interface with standard manipulation, sorting, and debugging features.

### Installation

```bash
$ npm install @fluentfixture/core
```

{% hint style="info" %}
The internals of the package and other utilities can be found on [streams](streams/ "mention") and [generators.md](generators.md "mention")sections.
{% endhint %}

### Example

Let us consider the following requirements. We need;

* One hundred products that are ordered by their prices.
* Each product has a code field with the "id-color" format calculated using generated values.
* Each product has the same category with "id" is 5.
* Half of them have stock.

```typescript
import { alphabetic, alphanumeric, bool, hex, int, obj, pick, val } from '@fluentfixture/core';

// Defines a price generator with amount and the currency fields.
const price = obj({
  amount: int(100, 1000),
  currency: pick(['USD', 'EUR', 'GBP', 'TRY']),
});

// Defines a color generator. (hex + pad + uppercase)
const color = hex(6).padStart(7, '#').upperCase();

// Defines a category with constant id.
const category = obj({
  id: val(5),
  code: alphanumeric().upperCase()
})

// Defines a product generator.
const product = obj({
  id: int(1, 999),
  name: alphabetic(10, 20).capitalCase(),
  category: category.memo(),
  description: alphabetic(20, 40).optional(),
  color: color,
  price: price,
  hasStock: bool(0.5),
});

// Adds 'code' field using generated values.
// Iterates the model.
// Sorts the generated models.
const products = product
  .lazy('code', (p) => `${p.id}-${p.color}`)
  .array(10)
  .sort((a, b) => a.price.amount - b.price.amount);

console.log(products.single());
```
