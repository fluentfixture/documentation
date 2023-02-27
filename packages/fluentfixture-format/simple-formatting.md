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

{% hint style="info" %}
The more information about pipes can be found on [pipe-functions](pipe-functions/ "mention")
{% endhint %}
