# String Generators

This section covers string-related generator functions.

<table>
   <thead>
      <tr>
         <th>Name</th>
         <th>Returns</th>
         <th data-type="checkbox">Deterministic</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td><a href="string-generators.md#text-str"><code>text()</code></a></td>
         <td><a href="../streams/string-stream.md"><code>StringStream</code></a></td>
         <td>true</td>
      </tr>
      <tr>
         <td><a href="string-generators.md#str-length"><code>str()</code></a></td>
         <td><a href="../streams/string-stream.md"><code>StringStream</code></a></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="string-generators.md#hex-length"><code>hex()</code></a></td>
         <td><a href="../streams/string-stream.md"><code>StringStream</code></a></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="string-generators.md#octal-length"><code>octal()</code></a></td>
         <td><a href="../streams/string-stream.md"><code>StringStream</code></a></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="string-generators.md#numeric-length"><code>numeric()</code></a></td>
         <td><a href="../streams/string-stream.md"><code>StringStream</code></a></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="string-generators.md#alphabetic-length"><code>alphabetic()</code></a></td>
         <td><a href="../streams/string-stream.md"><code>StringStream</code></a></td>
         <td>false</td>
      </tr>
      <tr>
         <td><a href="string-generators.md#alphanumeric-length"><code>alphanumeric()</code></a></td>
         <td><a href="../streams/string-stream.md"><code>StringStream</code></a></td>
         <td>false</td>
      </tr>
   </tbody>
</table>

## text (str)

Creates a [`StringStream`](../streams/string-stream.md) that generates always the given string.

| Name  | Description                 |
| ----- | --------------------------- |
| `str` | The string to be generated. |

```typescript
import { text } from '@fluentfixture/core';

console.log(text('str').single()); 
// prints always 'str'
```

## str (length)

Creates a [`StringStream`](../streams/string-stream.md) that generates an alphanumeric string with the given length.

| Name     | Description                                                          |
| -------- | -------------------------------------------------------------------- |
| `length` | The length of the string to be generated. The default value is `10`. |

```typescript
import { str } from '@fluentfixture/core';

console.log(str().single()); 
// prints an alphanumeric string
```

## hex (length)

Creates a [`StringStream`](../streams/string-stream.md) that generates a hexadecimal string with the given length.

| Name     | Description                                                          |
| -------- | -------------------------------------------------------------------- |
| `length` | The length of the string to be generated. The default value is `10`. |

```typescript
import { hex } from '@fluentfixture/core';

console.log(hex().single()); 
// prints a hexadecimal string
```

## binary (length)

Creates a [`StringStream`](../streams/string-stream.md) that generates a binary string with the given length.

| Name     | Description                                                          |
| -------- | -------------------------------------------------------------------- |
| `length` | The length of the string to be generated. The default value is `10`. |

```typescript
import { binary } from '@fluentfixture/core';

console.log(binary().single()); 
// prints a binary string
```

## octal (length)

Creates a [`StringStream`](../streams/string-stream.md) that generates an octal string with the given length.

| Name     | Description                                                          |
| -------- | -------------------------------------------------------------------- |
| `length` | The length of the string to be generated. The default value is `10`. |

```typescript
import { octal } from '@fluentfixture/core';

console.log(octal().single()); 
// prints an octal string
```

## numeric (length)

Creates a [`StringStream`](../streams/string-stream.md) that generates a  numeric string with the given length.

| Name     | Description                                                          |
| -------- | -------------------------------------------------------------------- |
| `length` | The length of the string to be generated. The default value is `10`. |

```typescript
import { numeric } from '@fluentfixture/core';

console.log(numeric().single()); 
// prints a numeric string
```

## alphabetic (length)

Creates a [`StringStream`](../streams/string-stream.md) that generates an  alphabetic string with the given length.

| Name     | Description                                                          |
| -------- | -------------------------------------------------------------------- |
| `length` | The length of the string to be generated. The default value is `10`. |

```typescript
import { alphabetic } from '@fluentfixture/core';

console.log(alphabetic().single()); 
// prints an alphabetic string
```

## alphanumeric (length)

Ceates a [`StringStream`](../streams/string-stream.md) that generates an alphanumeric string with the given length.

| Name     | Description                                                          |
| -------- | -------------------------------------------------------------------- |
| `length` | The length of the string to be generated. The default value is `10`. |

```typescript
import { alphanumeric } from '@fluentfixture/core';

console.log(alphanumeric().single()); 
// prints an alphanumeric string
```
