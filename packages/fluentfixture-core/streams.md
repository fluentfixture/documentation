# ⛓ Streams

> In software engineering, a fluent interface is an object-oriented API whose design relies extensively on method chaining. Its goal is to increase code legibility by creating a domain-specific language (DSL). (↪[wiki](https://en.wikipedia.org/wiki/Fluent\_interface))

In [@fluentfixture](../../), factories are small and valuable units, but they are very incapable of building complex and conditional data. Streams are factory wrappers (stream is a factory also) that provide a fluent interface. All methods of streams create other streams that wrap themselves. Like any factory, streams are also immutable and reusable types.
