# MathType Integration

JSDoc theme for [MathType JavaScript Integration API](https://github.com/wiris/mathtype-integration-js-dev).

Forked from [Bookshelf](https://github.com/wiris/bookshelf-jsdoc-theme/).


## Install

Clone repository to your designated `jsdoc` template directory:

```bash
$ git clone https://github.com/wiris/mathtype-integration-jsdoc-theme
```

## Usage

```bash
$ jsdoc entry-file.js -t path/to/mathtype-integration-jsdoc-theme
```

### Styles

Stlyes must be compiled if edited:

```bash
$ npm run styles
```

### Node.js Dependency

In your projects `package.json` file add a generate script:

```json
"script": {
  "generate-docs": "jsdoc --configure .jsdoc.json --verbose"
}

### Example JSDoc Config

```js
{
  "tags": {
    "allowUnknownTags": true,
    "dictionaries": ["jsdoc"]
  },
  "source": {
    "include": ["lib", "package.json", "README.md"],
    "includePattern": ".js$",
    "excludePattern": "(node_modules/|docs)"
  },
  "plugins": [
    "plugins/markdown"
  ],
  "templates": {
    "cleverLinks": false,
    "monospaceLinks": true
  },
  "opts": {
    "destination": "./docs/",
    "encoding": "utf8",
    "private": true,
    "recurse": true,
    "template": "path/to/mathtype-integration-jsdoc-theme"
    "whitelist": ['Optional', 'List', 'Of', 'Top', 'Level', 'Classes']
    "changelog": './path-to/CHANGELOG.md',
    "title": ""
  }
}
```

## License

Licensed under the GNU 3.0 General Public License.
