# Fluent Fixture

### Introduction

The **** [@fluentfixture](https://github.com/fluentfixture) **** is a flexible tool for generating customizable mock data with a fluent interface.

### **Philosophy**

> In Informatics, dummy data is benign information that does not contain any useful data, but serves to reserve space where real data is nominally present. Dummy data can be used as a placeholder for both testing and operational purposes. For testing, dummy data can also be used as stubs or pad to avoid software testing issues by ensuring that all variables and data fields are occupied. (↪[wiki](https://en.wikipedia.org/wiki/Dummy\_data))

In software development, generating mock data is a crucial necessity. In most cases, the test data quality directly impacts the development quality and velocity. But when it comes to generating conditional and complex mock data, things get a little more challenging. There are many dummy / mock / fixture data generators in the javascript ecosystem, but most have an unclean interface and limited capabilities.

The [@fluentfixture](https://github.com/fluentfixture) aims to provide a fluent interface and an extensible architecture. For this reason, the core of the package focuses on programmability, fluent interface, and extensibility.

{% hint style="info" %}
The [@fluentfixture](https://github.com/fluentfixture) does not provide predefined data like FakerJS for now. However, realistic data features will plan after the stable version of the core package, no-code support, and CLI.
{% endhint %}

### Packages

| Package                                                 | Desciption                                                     | Version |
| ------------------------------------------------------- | -------------------------------------------------------------- | ------- |
| [@fluentfixture/core](packages/fluentfixture-core/)     | Provides core modules and components for generating mock data. | `1.0.4` |
| [@fluentfixture/format](packages/fluentfixture-format/) | A flexible string format library.                              | `1.0.4` |

### License

@fluentfixture is [MIT](https://github.com/fluentfixture/fluentfixture/blob/main/LICENSE) licensed.
