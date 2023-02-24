# Structure

### Syntax

Formatting syntax consists of two parts: `${path:func1()|func2()|...|funcN()}`

* the `path` is the descriptor of the target property. When the `path` is empty, the target is the whole source object.
* the `func1()` , `func2()`, and the `funcN()` are pipe functions.

| Expression                  | Target Property | Pipe Functions          |
| --------------------------- | --------------- | ----------------------- |
| `${}`                       | `obj`           |                         |
| `${key}`                    | `obj.key`       |                         |
| `${key:trim()\|padLeft(5)}` | `obj.key`       | `trim()` , `padLeft(5)` |
| `${:trim()\|split(",")}`    | `obj`           | `trim()` , `split(",")` |

### Examples

[@fluentfixture/format](./) provides two global methods with the default configurations: `format` , `compile`. The `format` produces the formatted string immediately. Differently, `compile` returns a pre-compiled template for reuse.

#### Format

The `format` produces the formatted string immediately. Actually, the format compiles first, then executes the compiled template. For this reason, it is inefficient compared to the `compile`.

{% hint style="warning" %}
`compile` is fast than `format` especially repeating usages.
{% endhint %}

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

#### Compile

`compile` returns a pre-compiled template for reuse. Using the `compile` is extremely fast according to the `format` method for repeating usages.

```typescript
import { compile } from '@fluentfixture/format';

const template = compile('ID=${name}-${surname:upperCase()} > ${role.admin}');

template.format({
  name: 'albert',
  surname: 'einstein',
  role: {
    admin: true
  }
});
// ID=albert-EINSTEIN > true

template.format({
  name: 'nikola',
  surname: 'tesla',
  role: {
    admin: false
  }
});
// ID=nikola-TESLA > false
```
