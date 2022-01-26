# Fluent Fixture

## Introduction

The **** FluentFixture **** is a flexible tool for generating customizable mock data with a fluent interface.

## **Philosophy**

> In Informatics, dummy data is benign information that does not contain any useful data, but serves to reserve space where real data is nominally present. Dummy data can be used as a placeholder for both testing and operational purposes. For testing, dummy data can also be used as stubs or pad to avoid software testing issues by ensuring that all variables and data fields are occupied. (↪[wiki](https://en.wikipedia.org/wiki/Dummy\_data))

In software development, generating mock data is a crucial necessity. In most cases, the test data quality directly impacts the development quality and velocity. But when it comes to generating conditional and complex mock data, things get a little more challenging. There are many dummy / mock / fixture data generators in the javascript ecosystem, but most have an unclean interface and limited capabilities.

The FluentFixture aims to provide a fluent interface and an extensible architecture. For this reason, the core of the package focuses on programmability, fluent interface, and extensibility.

{% hint style="info" %}
The FluentFixture does not provide predefined data like FakerJS for now. However, realistic data features will plan after the stable version of the core package, no-code support, and CLI.
{% endhint %}

## Getting started

To get started, install the dependencies with **npm** (or **yarn**) or clone the repository.

{% tabs %}
{% tab title="Install via NPM" %}
```
$ npm install @fluentfixture/core
```
{% endtab %}

{% tab title="Install via Yarn" %}
```
$ yarn add @fluentfixture/core
```
{% endtab %}

{% tab title="Clone repository" %}
```
$ git clone git@github.com:fluentfixture/fluentfixture.git
```
{% endtab %}
{% endtabs %}
