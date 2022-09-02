# ❗ Error Handling

In the formatting process, there may be two types of errors.

* Syntax errors.
* Transformation errors.

### Syntax Errors

Syntax errors are always thrown. The following templates are invalid.

```typescript
import { format } from '@fluentfixture/format';

format('${name:}', {}); // missing transformers.
format('${name:padStart}', {}); // missing parameters.
format('${padStart()}', {}); // missing semicolon at the index 0.
format("${:split(',')}", {}); // single quotes are not supported.
```

### Transformation Errors

Transformation errors occur while invoking a transformation method. By default, these kinds of errors are handled by the library.

#### With IgnoreErrors Flag

```typescript
import { Formatter, Pipes } from '@fluentfixture/format';

const formatter = Formatter.create(Pipes.withDefaults(), { ignoreErrors: true });

formatter.format('ITEMS = ${items:join("+")}', { });
// ITEMS = 
```

#### Without IgnoreErrors Flag

```typescript
import { Formatter, Pipes } from '@fluentfixture/format';

const formatter = Formatter.create(Pipes.withDefaults(), { ignoreErrors: false });

formatter.format('ITEMS = ${items:join("+")}', { });
// TypeError: Cannot read properties of undefined (reading 'join')

```
