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

### Example

[@fluentfixture/format](./) provides two global methods and one default instance with default configurations: `format` , `compile`, and the `formatter`. The `format` produces the formatted string immediately. Differently, `compile` returns a pre-compiled template for reuse.

{% hint style="info" %}
Using the `compile` is extremely fast according to the `format` method for repeating usages.
{% endhint %}

```typescript
import { format, compile, formatter } from '@fluentfixture/format';

const source = {
  name: 'john',
  surname: 'doe',
  balance: {
    amount: 120,
    currency: 'USD'
  },
  memberships: ['regular user', 'pro user']
};

format('${name:capitalCase()}.${surname:upperCase()} > MEMBERSHIP=${memberships.0:dotCase()}', source);
// returns "John.DOE > MEMBERSHIP=regular.user"

const template = compile('${name:capitalCase()}.${surname:upperCase()} > MEMBERSHIP=${memberships.0:dotCase()}');

template(source);
// returns "John.DOE > MEMBERSHIP=regular.user"
```
