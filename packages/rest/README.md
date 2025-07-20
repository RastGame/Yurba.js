<div align="center">
  <br />
  <p>
    <a href="https://yurba.js.org"><img src="https://yurba.js.org/banner.svg" width="500" alt="yurba.js logo" /></a>
  </p>
  <br />
  <p>
    <a href="https://www.npmjs.com/package/@yurbajs/rest"><img src="https://img.shields.io/npm/v/@yurbajs/rest.svg?maxAge=3600" alt="npm version" /></a>
    <a href="https://www.npmjs.com/package/@yurbajs/rest"><img src="https://img.shields.io/npm/dt/@yurbajs/rest.svg?maxAge=3600" alt="npm downloads" /></a>
    <a href="https://github.com/yurbajs/yurba.js/commits/main"><img src="https://img.shields.io/github/last-commit/yurbajs/yurba.js.svg?logo=github&logoColor=ffffff" alt="Last commit" /></a>
    <a href="https://www.npmjs.com/package/@yurbajs/rest"><img src="https://img.shields.io/npm/last-update/@yurbajs/rest" alt="npm last update"></a>
  </p>
</div>

## About
REST client for Yurba API with full TypeScript support.

> WARNING: it's alpha version 

## Install
Node.js 20 or newer is required.

```sh
npm install @yurbajs/rest
yarn add @yurbajs/rest
pnpm add @yurbajs/rest
bun add @yurbajs/rest
```

## Example usage

```js
import { REST } from '@yurbajs/rest';

const api = new REST('TOKEN');

try {
  // Get user info
  const user = await api.users.getMe();
  console.log('Bot user:', user);

  // Send message (dialogid)
  try {
    const message = await api.messages.send(1111, 'Hello, world!');
    console.log('Message sent:', message);
  } catch (error) {
    console.error('Failed to send message:', error.message);
  }

  // Get user by tag (@)
  try {
    const targetUser = await api.users.getByTag('rastgame');
    console.log('User:', targetUser);
  } catch (error) {
    console.error('Failed to get user:', error.message);
  }
} catch (error) {
  console.error('Failed to get bot info:', error.message);
}
```

## Links

* [Website][website] ([source][website-source])
* [Documentation][documentation]
* [Yurba Account][yurba]
* [Yurba Channel][yurba-channel]
* [Yurba Chat][yurba-chat]
* [GitHub][source]
* [npm][npm]

## Contributing

Want to help make yurba.js better?

* Found a bug? [Open an issue](https://github.com/yurbajs/yurba.js/issues/new).
* Have an idea? [Start a discussion](https://github.com/yurbajs/yurba.js/discussions).
* Want to contribute code? Fork the repository and submit a pull request.

Please make sure to follow our coding style and test your changes before submitting.

## Getting Help

Need assistance?

* Check the [documentation][documentation] first.
* Ask questions in our [Chat][yurba-chat].
* Browse existing [issues](https://github.com/yurbajs/yurba.js/issues) and [discussions](https://github.com/yurbajs/yurba.js/discussions).

[source]: https://github.com/yurbajs/yurba.js/tree/main/packages/rest
[website]: https://yurba.js.org
[website-source]: https://github.com/yurbajs/yurba.js
[documentation]: https://yurba.js.org/docs
[yurba]: https://me.yurba.one/yurbajs
[yurba-channel]: https://me.yurba.one/yjs
[yurba-chat]: https://me.yurba.one/yurba.js
[npm]: https://www.npmjs.com/package/@yurbajs/rest