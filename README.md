# MathType Integration

JSDoc theme for [MathType JavaScript Integration API](https://www.npmjs.com/package/@wiris/mathtype-html-integration-devkit).

Forked from [Bookshelf](https://github.com/wiris/bookshelf-jsdoc-theme/).

## Install Instructions

Clone the [MathType Javascript Integration API](https://www.npmjs.com/package/@wiris/mathtype-html-integration-devkit) from the MathType web repository:

```bash
$ git clone https://github.com/wiris/html-integrations
$ cd packages/mathtype-html-integration-devkit
```

Then, install `npm` dependencies:

```bash
$ npm install
```
## Usage

Run this commands to generate the source files of the documentation site:

```bash
$ npm run build-docs
```
The source code of the documentation site is generated on the `/out` folder.

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
