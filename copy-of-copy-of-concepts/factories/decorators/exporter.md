# Exporter

[`Exporter`](broken-reference) decorator decorates a factory with the exporter function. When the `single()` method is invoked, it generates data using the decorated factory and passes the result into the given function as input, then returns the same result.

| Name      | Description                            |
| --------- | -------------------------------------- |
| `factory` | The factory to be decorated.           |
| `fn`      | The function that receives the result. |

{% hint style="info" %}
[`Exporter`](broken-reference) decorator is used with [streams](broken-reference) mainly. Advanced examples can be found in the [debugging](../../../fundamentals/debugging.md) section.
{% endhint %}

## Example

```typescript
// example
```
