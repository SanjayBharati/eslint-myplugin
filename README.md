# eslint-plugin-myplugin

eslint plugin for myplugin

## Installation

You'll first need to install [ESLint](http://eslint.org):

```
$ npm i eslint -g
```

Next, install `eslint-plugin-myplugin`:

```
$ npm install eslint-plugin-myplugin -g
```

**Note:** If you installed ESLint globally (using the `-g` flag) then you must also install `eslint-plugin-myplugin` globally.

## Usage

Add `sm` to the plugins section of your `.eslintrc` configuration file. You can omit the `eslint-plugin-` prefix:

```json
{
    "plugins": [
        "sm"
    ]
}
```


Then configure the rules you want to use under the rules section. For now, the fix only support `"always"` option.

```json
{
    "rules": {
        "sm/no-tabs": "error",
        "newline-after-var": "off",
        "sm/newline-after-var": ["error", "always"]
    }
}
```
## Example 

with shareable config:  [eslint-config-myplugin](https://www.npmjs.com/package/eslint-config-myplugin) and this plugin:

```
{
    root: true,
    "plugins": [
        "sm"
    ],
    "rules": {
        "sm/no-tabs": "error",
        "newline-after-var": "off",
        "sm/newline-after-var": ["error", "always"]
    },
    extends: "sm"
}

```