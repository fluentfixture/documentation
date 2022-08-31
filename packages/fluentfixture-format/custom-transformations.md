# Custom Transformations

[@fluentfixture/format](./) supports custom transformation functions. When customization is needed, a new instance can be used.

```typescript
import { Formatter, Pipes } from '@fluentfixture/format';

const source = {
  balance: {
    amount: 12, 
    currency: 'TRY'
  }
};

const pipes = Pipes.withDefaults()
  .register('inc', (val: number, arg: number) => val + arg)
  .register('amount', (val: any) => `[${value.amount} ${value.currency}]`);

const formatter = Formatter.create(pipes);

formatter.format('BALANCE=${balance:amount()}', source);
// returns "BALANCE=12 TRY"

formatter.format('NEXT AMOUNT=${balance.amount:inc(10)}', source);
// returns "NEXT AMOUNT="22
```
