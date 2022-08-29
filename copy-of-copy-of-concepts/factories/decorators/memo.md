# Memo

> In computing, memoization or memoisation is an optimization technique used primarily to speed up computer programs by storing the results of expensive function calls and returning the cached result when the same inputs occur again. (↪[wiki](https://en.wikipedia.org/wiki/Memoization))

[`Memo`](broken-reference) decorator decorates a factory with the memoization function. When the `single()` method is invoked, it generates data and stores it in the memoization function; after that, always return the stored result.

| Name      | Description                  |
| --------- | ---------------------------- |
| `factory` | The factory to be decorated. |

{% hint style="info" %}
[`Memo`](broken-reference) decorator is used with [streams](broken-reference) mainly. Advanced examples can be found in the [optimization](../../../fundamentals/optimization.md) section.
{% endhint %}

## Example

```typescript
// example
```
