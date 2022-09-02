# 🐣 Customs

[@fluentfixture/format](../) comes with lots of default transformation functions. In addition to these, custom providers can be defined.

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
  .register('amount', (val: any) => `[${val.amount} ${val.currency}]`);

const formatter = Formatter.create(pipes);

formatter.format('BALANCE=${balance:amount()}', source);
// BALANCE=[12 TRY]

formatter.format('NEXT AMOUNT=${balance.amount:inc(10)}', source);
// NEXT AMOUNT=22
```
