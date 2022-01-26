# Generate your first mock data

```typescript
import { num, obj, pick } from '@fluentfixture/core';

const price = obj({
  amount: num(0.01, 9.99),
  currency: pick(['USD', 'EUR', 'GBP', 'TRY'])
});
```
