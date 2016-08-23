#  [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][daviddm-image]][daviddm-url] [![Coverage Status][coveralls-image]][coveralls-url]

[![Join the chat at https://gitter.im/conventional-changelog/conventional-changelog](https://badges.gitter.im/conventional-changelog/conventional-changelog.svg)](https://gitter.im/conventional-changelog/conventional-changelog?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

> Generate a changelog from git metadata

It's recommended to use high level [standard-version](https://github.com/conventional-changelog/standard-version).
Alternatively, you are probably looking for the [cli](https://github.com/conventional-changelog/conventional-changelog-cli) module.
Or use one of the plugins if you are already using the tool:  [grunt](https://github.com/btford/grunt-conventional-changelog)/[gulp](https://github.com/conventional-changelog/gulp-conventional-changelog)/[atom](https://github.com/conventional-changelog/atom-conventional-changelog).


## Usage

```sh
$ npm install --save conventional-changelog
```

```js
var conventionalChangelog = require('conventional-changelog');

conventionalChangelog({
  preset: 'angular'
})
  .pipe(process.stdout); // or any writable stream
```


## API

### conventionalChangelog([options, [context, [gitRawCommitsOpts, [parserOpts, [writerOpts]]]]])

Returns a readable stream.

#### options

See the [conventional-changelog-core](https://github.com/conventional-changelog/conventional-changelog-core) docs. The API is the same with the following changes or additions:

##### preset

Type: `string` Possible values: `'angular', 'atom', 'codemirror', 'ember', 'eslint', 'express', 'jquery', 'jscs', 'jshint'`

It's recommended to use a preset so you don't have to define everything yourself. Presets are names of built-in `config`.

**NOTE:** `options.config` will be overwritten by the values of preset. You should use either `preset` or `config`, but not both.


## [Notes for parent modules](https://github.com/conventional-changelog/conventional-changelog-core#notes-for-parent-modules)


## Related

- [conventional-changelog-cli](https://github.com/conventional-changelog/conventional-changelog-cli) - cli of this module
- [standard-changelog](https://github.com/conventional-changelog/standard-changelog) - Similar to this module but only with angular convention
- [conventional-github-releaser](https://github.com/conventional-changelog/conventional-github-releaser) - Make a new GitHub release from git metadata
- [conventional-recommended-bump](https://github.com/conventional-changelog/conventional-recommended-bump) - Get a recommended version bump based on conventional commits
- [conventional-commits-detector](https://github.com/conventional-changelog/conventional-commits-detector) - Detect what commit message convention your repository is using
- [commitizen](https://github.com/commitizen/cz-cli) - Simple commit conventions for internet citizens.
- [angular-precommit](https://github.com/ajoslin/angular-precommit) - Pre commit with angular conventions
- [conventional-changelog-lint](https://github.com/marionebl/conventional-changelog-lint) - Lint commit messages against your conventional-changelog preset


## License

MIT


[npm-image]: https://badge.fury.io/js/conventional-changelog.svg
[npm-url]: https://npmjs.org/package/conventional-changelog
[travis-image]: https://travis-ci.org/conventional-changelog/conventional-changelog.svg?branch=master
[travis-url]: https://travis-ci.org/conventional-changelog/conventional-changelog
[daviddm-image]: https://david-dm.org/conventional-changelog/conventional-changelog.svg?theme=shields.io
[daviddm-url]: https://david-dm.org/conventional-changelog/conventional-changelog
[coveralls-image]: https://coveralls.io/repos/conventional-changelog/conventional-changelog/badge.svg
[coveralls-url]: https://coveralls.io/r/conventional-changelog/conventional-changelog
