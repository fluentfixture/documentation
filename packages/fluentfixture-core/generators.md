# 💎 Generators

In [@fluentfixture](../../), streams cannot be initialized directly. To take advantage of the stream's fluent interface, we can use generator functions.

### Booleans

#### bool()

Returns a [`BooleanStream`](streams/booleanstream.md)  that produces a boolean value.

<table><thead><tr><th>Parameter</th><th data-type="select">Type</th><th>Default</th><th>Description</th></tr></thead><tbody><tr><td>percentage</td><td></td><td><code>0.5</code></td><td>Produce a boolean with the specified chance causing it to be <code>true</code></td></tr></tbody></table>

#### truthy()

Returns a [`BooleanStream`](streams/booleanstream.md)  that always produces `true`.

#### falsy()

Returns a [`BooleanStream`](streams/booleanstream.md)  that always produces `false`.
