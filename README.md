# babel-plugin-project-relative-require

[![npm version](https://badge.fury.io/js/babel-plugin-project-relative-require.svg)](https://badge.fury.io/js/babel-plugin-project-relative-require)

A Bable plugin for importing modules relative to the current working directory
(cwd).
Idea taken from FakeRainBrigand answer http://stackoverflow.com/a/31069137/1329668


## Example

**In**

```javascript
import myModule from 'cwd://mymyModule';
```

**Out**

```javascript
import myModule from '<relative_path_from_your_current_place>mymyModule';
```

## Installation

```sh
$ npm install babel-plugin-project-relative-require
```

## Usage

### Via `.babelrc` (Recommended)

**.babelrc**

```json
{
  "plugins": ["babel-plugin-project-relative-require"]
}
```

## Via CLI

```sh
$ babel --plugins babel-plugin-project-relative-require script.js
```

### Via Node API

```javascript
require("babel-core").transform("code", {
  plugins: ["babel-plugin-project-relative-require"]
});
```
