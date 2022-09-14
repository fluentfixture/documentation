# Fluent Fixture

<figure><img src=".gitbook/assets/logo.jpeg" alt=""><figcaption></figcaption></figure>

The **** [@fluentfixture](https://github.com/fluentfixture) **** is a flexible tool for generating customizable mock data with a fluent interface 🚀

[![NPM Version](https://camo.githubusercontent.com/dadffe9bc1f0150a737c7c7c923713e49fe159ff54bcbc0b465e70716fba80f9/68747470733a2f2f696d672e736869656c64732e696f2f6e706d2f762f40666c75656e74666978747572652f636f72652e737667)](https://www.npmjs.com/package/@fluentfixture/core) [![Package License](https://camo.githubusercontent.com/946e10f97a0a619e3176feb46fe56b88579bc3a6e1a77c7720160ce29d01b41f/68747470733a2f2f696d672e736869656c64732e696f2f6e706d2f6c2f40666c75656e74666978747572652f636f72652e737667)](https://www.npmjs.com/package/@fluentfixture/core) [![CircleCI](https://camo.githubusercontent.com/c23730fb2f12b7599344cc4d4daa71114c89aebeaba74636870db632ac7f2c72/68747470733a2f2f646c2e636972636c6563692e636f6d2f7374617475732d62616467652f696d672f67682f666c75656e74666978747572652f666c75656e74666978747572652f747265652f6d61696e2e7376673f7374796c653d737667)](https://dl.circleci.com/status-badge/redirect/gh/fluentfixture/fluentfixture/tree/main) [![Coverage](https://camo.githubusercontent.com/89c9c645bf79be82701a0809623719c33ea8d175b12060a316fff1fb0004996f/68747470733a2f2f636f766572616c6c732e696f2f7265706f732f6769746875622f666c75656e74666978747572652f666c75656e74666978747572652f62616467652e7376673f6272616e63683d6d61696e2339)](https://coveralls.io/github/fluentfixture/fluentfixture?branch=main) [![Known Vulnerabilities](https://camo.githubusercontent.com/936cff7898ebb4d601599026c59677c0ef18fed048dfbab5a365787e1d87830a/68747470733a2f2f736e796b2e696f2f746573742f6769746875622f666c75656e74666978747572652f666c75656e74666978747572652f62616467652e737667)](https://snyk.io/test/github/fluentfixture/fluentfixture) [![CodeFactor](https://camo.githubusercontent.com/b48f5ee7f5d0a5249a763e600ae4445fb23f412fa3ba1384379921d350b336d9/68747470733a2f2f7777772e636f6465666163746f722e696f2f7265706f7369746f72792f6769746875622f666c75656e74666978747572652f666c75656e74666978747572652f6261646765)](https://www.codefactor.io/repository/github/fluentfixture/fluentfixture) [![Open in CodeSandbox](https://camo.githubusercontent.com/fea481e068f26e251350b77807052bdb6dfe8e5afc0059a724afe97e3d5da103/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4f70656e253230696e2d436f646553616e64626f782d626c75653f7374796c653d666c61742d737175617265266c6f676f3d636f646573616e64626f78)](https://codesandbox.io/s/github/fluentfixture/fluentfixture/tree/main/sample/02-core) [![Open in CodeSandbox](https://camo.githubusercontent.com/91c5d0d2bfbd8d6b4f6e4cd5ee78681dbdd3fe5b1addaf6024ed478847b7f9f9/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4f70656e253230696e2d476974426f6f6b2d79656c6c6f773f7374796c653d666c61742d737175617265266c6f676f3d676974626f6f6b)](https://docs.fluentfixture.com/)

### **Philosophy**

> In Informatics, dummy data is benign information that does not contain any useful data, but serves to reserve space where real data is nominally present. Dummy data can be used as a placeholder for both testing and operational purposes. For testing, dummy data can also be used as stubs or pad to avoid software testing issues by ensuring that all variables and data fields are occupied. (↪[wiki](https://en.wikipedia.org/wiki/Dummy\_data))

In software development, generating mock data is a crucial necessity. In most cases, the test data quality directly impacts the development quality and velocity. But when it comes to generating conditional and complex mock data, things get a little more challenging. There are many dummy / mock / fixture data generators in the javascript ecosystem, but most have an unclean interface and limited capabilities.

The [@fluentfixture](https://github.com/fluentfixture) aims to provide a fluent interface and an extensible architecture. For this reason, the core of the package focuses on programmability, fluent interface, and extensibility.

{% hint style="info" %}
The [@fluentfixture](https://github.com/fluentfixture) does not provide predefined data like FakerJS for now. However, realistic data features will plan after the stable version of the core package, no-code support, and CLI.
{% endhint %}

### Packages

* [#core-fluentfixture-core](./#core-fluentfixture-core "mention")
* [#format-fluentfixture-format](./#format-fluentfixture-format "mention")

### 🔥Core (@fluentfixture/core)

[@fluentfixture/core](packages/fluentfixture-core/) provides core modules and components for generating mock data.

#### Installation

```bash
$ npm install @fluentfixture/core
```

#### Usage

[![Open in CodeSandbox](https://camo.githubusercontent.com/fea481e068f26e251350b77807052bdb6dfe8e5afc0059a724afe97e3d5da103/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4f70656e253230696e2d436f646553616e64626f782d626c75653f7374796c653d666c61742d737175617265266c6f676f3d636f646573616e64626f78)](https://codesandbox.io/s/github/fluentfixture/fluentfixture/tree/main/sample/02-core) [![Open in GitHub](https://camo.githubusercontent.com/2cc17ac141e499106ea5630a4effeba323c90f01b700f5d51cf223b0fd56ed83/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4f70656e253230696e2d4769746875622d677265656e3f7374796c653d666c61742d737175617265266c6f676f3d676974687562)](https://github.com/fluentfixture/fluentfixture/tree/main/sample/02-core) [![Open in GitBook](https://camo.githubusercontent.com/91c5d0d2bfbd8d6b4f6e4cd5ee78681dbdd3fe5b1addaf6024ed478847b7f9f9/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4f70656e253230696e2d476974426f6f6b2d79656c6c6f773f7374796c653d666c61742d737175617265266c6f676f3d676974626f6f6b)](https://docs.fluentfixture.com/packages/fluentfixture-core)

```typescript
import { alphabetic, bool, hex, int, obj, pick } from '@fluentfixture/core';

// Defines a price generator with amount and the currency fields.
const price = obj({
  amount: int(1, 100), // generates an integer between 1 and 100
  currency: pick(['USD', 'EUR', 'GBP', 'TRY']), // picks one of them
});

// Defines a color generator. (hex + pad + uppercase)
const color = hex(6).padStart(7, '#').upperCase(); 

// Defines a product generator.
const product = obj({
  id: int(1, 999), // generates an integer between 1 and 999
  name: alphabetic(20).capitalCase(), // generates a name with capital case
  color: color, // generates color by using the color generator
  price: price, // generates price by using the price generator
  discount: price.optional(), // generates price by using the price generator or undefined
  featured: bool(0.7), // generates a boolean that mostly true
});

// Introduces the 'code' field using the previously generated id and the color.
// By doing this, all mock products are consistent within themselves.
const productWithCode = product
  .lazy('code', (p) => `${p.id}-${p.color}`);

// Converts productWithCode generator to an array and sort them by using the id field.
const products = productWithCode
  .array(10)
  .sort((a, b) => a.id - b.id);

// Executes the model.
console.log(products.single());
```

### 💎Format (@fluentfixture/format)

[@fluentfixture/format](packages/fluentfixture-format/) provides formatting and compiling functionalities with extensible transformation capabilities.

#### Installation

```bash
$ npm install @fluentfixture/format
```

#### Usage

[![Open in CodeSandbox](https://camo.githubusercontent.com/fea481e068f26e251350b77807052bdb6dfe8e5afc0059a724afe97e3d5da103/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4f70656e253230696e2d436f646553616e64626f782d626c75653f7374796c653d666c61742d737175617265266c6f676f3d636f646573616e64626f78)](https://codesandbox.io/s/github/fluentfixture/fluentfixture/tree/main/sample/01-format) [![Open in GitHub](https://camo.githubusercontent.com/2cc17ac141e499106ea5630a4effeba323c90f01b700f5d51cf223b0fd56ed83/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4f70656e253230696e2d4769746875622d677265656e3f7374796c653d666c61742d737175617265266c6f676f3d676974687562)](https://github.com/fluentfixture/fluentfixture/tree/main/sample/01-format) [![Open in GitBook](https://camo.githubusercontent.com/91c5d0d2bfbd8d6b4f6e4cd5ee78681dbdd3fe5b1addaf6024ed478847b7f9f9/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4f70656e253230696e2d476974426f6f6b2d79656c6c6f773f7374796c653d666c61742d737175617265266c6f676f3d676974626f6f6b)](https://docs.fluentfixture.com/packages/fluentfixture-format)

```typescript
import { format } from '@fluentfixture/format';

const source = {
  name: 'john',
  surname: 'doe',
  birthdate: new Date(1_617_258_460_000), // GMT: Thursday, 1 April 2021 06:27:40
};

// format() returns a formatted string immediately.
console.log(
  format('${surname:upperCase()}, ${name:capitalCase()} BIRTH_DATE=${birthdate:date("MM-DD-YYYY")}', source),
);

// compile() returns a pre-compiled template for reusing.
const template = compile('${name:capitalCase()}, ${age:default("N/A")} >> ${colors:join("+")}');

console.log(
  template.format({
    name: 'john',
    age: 32,
    colors: ['red', 'black']
  })
);
```

### License

@fluentfixture is [MIT](https://github.com/fluentfixture/fluentfixture/blob/main/LICENSE) licensed.
