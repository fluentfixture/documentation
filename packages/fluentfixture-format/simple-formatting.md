# Structure

### Syntax

Formatting syntax consists of two parts: `${path:func1()|func2()|...|funcN()}`

* the `path` is the descriptor of the target property. When the `path` is empty, the target is the whole source object.
* the `func1()` , `func2()`, and the `funcN()` are pipe functions.

<table><thead><tr><th width="335.3333333333333">Expression</th><th width="169">Target Property</th><th>Pipe Functions</th></tr></thead><tbody><tr><td><code>${}</code></td><td><code>obj</code></td><td></td></tr><tr><td><code>${key}</code></td><td><code>obj.key</code></td><td></td></tr><tr><td><code>${key:trim()|padLeft(5)}</code></td><td><code>obj.key</code></td><td><code>trim()</code> , <code>padLeft(5)</code></td></tr><tr><td><code>${:trim()|split(",")}</code></td><td><code>obj</code></td><td><code>trim()</code> , <code>split(",")</code></td></tr></tbody></table>

{% hint style="info" %}
The more information about pipes can be found on [pipe-functions](pipe-functions/ "mention")
{% endhint %}
