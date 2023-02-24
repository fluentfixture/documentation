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
