# Fluent Fixture

The [@fluentfixture](https://github.com/fluentfixture) is a flexible tool for generating customizable mock data with a fluent interface.

## **Philosophy**

> In Informatics, dummy data is benign information that does not contain any useful data, but serves to reserve space where real data is nominally present. 
> Dummy data can be used as a placeholder for both testing and operational purposes. 
> For testing, dummy data can also be used as stubs or pad to avoid software testing issues by ensuring that all variables and data fields are occupied. (↪[wiki](https://en.wikipedia.org/wiki/Dummy\_data))

Generating dummy data is crucial in software development. The quality of test data directly impacts development quality and velocity.
There are many dummy data generators in the JavaScript ecosystem. However, creating complex objects and responding to real-world use cases can be challenging.

The [@fluentfixture](https://github.com/fluentfixture) aims to provide a fluent interface and an extensible architecture for generating dummy data.

{% hint style="info" %}
The [@fluentfixture](https://github.com/fluentfixture) doesn't provide predefined data like FakerJS but offers multiple adapters for integration with external libraries.
{% endhint %}

## Packages

### Core (@fluentfixture/core)

The [@fluentfixture/core](https://docs.fluentfixture.com/packages/fluentfixture-core) provides various data generators for different use cases.
All generators offer a fluent interface for manipulating data, including sorting, creating conditional values, and more.

***

### Format (@fluentfixture/format)

The [@fluentfixture/format](https://docs.fluentfixture.com/packages/fluentfixture-format) is a flexible string format library that provides formatting functionality with extensible formatting capability.

## License

@fluentfixture is [MIT](https://github.com/fluentfixture/fluentfixture/blob/main/LICENSE) licensed.
