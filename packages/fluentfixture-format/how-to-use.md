# How To Use

### Global Methods

The `compile` and `format` are two global methods of the [@fluentfixture/format](./) package. Global methods have default configurations and cannot be modified.

#### Compile

The `compile` method compiles the template for reusability. Pre-compiled templates extremely fast according to the `format` method for repeating usages. It doesn't require a source object during the compilation process.

```typescript
import { compile } from '@fluentfixture/format';

const template = compile('${name:capitalCase()}, ${age:default("N/A")} >> ${colors:join("+")}');

template.format({
  name: 'john',
  age: 32,
  colors: ['red', 'black']
});
// "John, 32 >> red+black"

template.format({
  name: 'john',
  surname: 'doe'
});
// "John, N/A >> "  

template.format({
  name: 'john',
  admin: false,
  age: 11,
  colors: ['blue']
});
// "John, 11 >> blue"
```

#### Format

The `format` method converts the template and the source object directly to a string.

```typescript
import { format } from '@fluentfixture/format';

const source = {
  name: 'john',
  surname: 'doe',
  balance: {
    amount: 120,
    currency: 'USD'
  },
  memberships: ['regular', 'starter']
};

format('${name:capitalCase()}.${surname:upperCase()} > MEMBERSHIP-1=${memberships.0}', source);
// John.DOE > MEMBERSHIP-1=regular


format('${surname:upperCase()|padEnd(5, "#")} > MEMBERSHIPS=${memberships:join("+")}', source);
// DOE## > MEMBERSHIPS=regular+starter
```

### Formatter Instance

For advanced use cases, a new `Formatter` instance can be used. New instance can be useful, especially for modifying or extendingn the built-in pipe functions.

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
