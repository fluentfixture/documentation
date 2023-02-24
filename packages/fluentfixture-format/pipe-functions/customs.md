# Custom Pipes

### Registering Custom Pipes

In addition to built-in pipes, any number of custom pipes can be defined. A pipe must be a function with at least one parameter. The leftmost parameter of the pipe function will be used to retrive the previous output.

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
