# Stream

The `Stream` is the base class of all streams.

### Instance Methods

#### single()

Returns the produced value.

{% hint style="info" %}
This method ends the stream flow.
{% endhint %}

#### many()

Returns the produced array.

{% hint style="info" %}
This method ends the stream flow.
{% endhint %}

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td>length</td><td></td><td><code>10</code></td><td>The length of the output.</td></tr></tbody></table>

#### array()

Returns an [`ArrayStream`](arraystream.md) with the given length.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td>length</td><td></td><td><code>10</code></td><td>The length of the new <code>ArrayStream</code>.</td></tr></tbody></table>
