# package-json [![Build Status](https://travis-ci.org/sindresorhus/package-json.svg?branch=master)](https://travis-ci.org/sindresorhus/package-json)

> Get the package.json of a package from the npm registry


## Install

```
$ npm install --save package-json
```


## Usage

```js
const packageJson = require('package-json');

packageJson('pageres', 'latest').then(json => {
	console.log(json);
	//=> {name: 'pageres', ...}
});

// also works with scoped packages
packageJson('@company/package', 'latest').then(json => {
	console.log(json);
	//=> {name: 'package', ...}
});
```


## API

### packageJson(name, [version])

You can optionally specify a version (e.g. `1.0.0`) or `latest`.  
If you don't specify a version you'll get the [main entry](http://registry.npmjs.org/pageres/) containing all versions.


## Related

- [latest-version](https://github.com/sindresorhus/latest-version) - Get the latest version of a npm package
- [npm-keyword](https://github.com/sindresorhus/npm-keyword) - Get a list of npm packages with a certain keyword
- [npm-user](https://github.com/sindresorhus/npm-user) - Get user info of a npm user
- [npm-email](https://github.com/sindresorhus/npm-email) - Get the email of a npm user


## License

MIT © [Sindre Sorhus](http://sindresorhus.com)
