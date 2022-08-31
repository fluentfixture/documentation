# Simple Formatting

### Syntax

Formatting syntax consists of two parts: `${path:pipe-1|pipe-2|...|pipe-n}`

* the `path` is the descriptor of the target property. When the `path` is empty, the target is the whole source object.
* the `pipe-1` , `pipe-2`, and the `pipe-n` are transformation functions.

| Syntax                      | Target    | Transformations         |
| --------------------------- | --------- | ----------------------- |
| `${}`                       | `obj`     |                         |
| `${key}`                    | `obj.key` |                         |
| `${key:trim()\|padLeft(5)}` | `obj.key` | `trim()` , `padLeft(5)` |
| `${:trim()\|split(",")}`    | `obj`     | `trim()` , `split(",")` |

### Examples

[@fluentfixture/format](./) provides two global methods and one default instance with default configurations: `format` , `compile`, and the `formatter`. The `format` produces the formatted string immediately. Differently, `compile` returns a pre-compiled template for reuse.

#### Format Example

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

#### Compile Example

{% hint style="info" %}
Using the `compile` is extremely fast according to the `format` method for repeating usages.
{% endhint %}

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
