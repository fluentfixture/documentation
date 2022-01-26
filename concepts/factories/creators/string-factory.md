# String Factory

[`StringFactory`](string-factory.md) generates a `string` by using the given charset and length.

| Name      | Description                                |
| --------- | ------------------------------------------ |
| `charset` | The charset of the string to be generated. |
| `length`  | The length of the string to be generated.  |

{% hint style="info" %}
[`StringFactory`](string-factory.md) uses [`randomstring`](https://www.npmjs.com/package/randomstring) package for generating streams.
{% endhint %}

## Charsets

[`StringFactory`](string-factory.md) support the following charsets:

| Charset        | Output                |
| -------------- | --------------------- |
| `hex`          | `[0-9a-f]`            |
| `octal`        | `[0-7]`               |
| `numeric`      | `[0-9]`               |
| `binary`       | `[0-1]`               |
| `alphanumeric` | `[0-9a-zA-Z]`         |
| `alphabetic`   | `[a-zA-Z]`            |
| `custom`       | Any given characters. |

## Example

```typescript
// example
```
