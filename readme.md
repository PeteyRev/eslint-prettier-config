# Eslint and Prettier Setup with VSCode
A portable eslint/prettier config setup with vscode. 

## Installation

1. If you don't already have a `package.json` file, create one with `npm init`.

2. Then we need to install everything needed by the config:

```
npx install-peerdeps --dev eslint-config-pete
```

3. You can see in your package.json there are now a big list of devDependencies.

4. Create a `.eslintrc` file in the root of your project's directory (it should live where package.json does). Your `.eslintrc` file should look like this:

```
{
  "extends": [
    "pete"
  ]
}
```
5. Update VSCode settings:
```
	"editor.formatOnSave": true,
	// turn it off for JS and JSX, we will do this via eslint
	"[javascript]": {
		"editor.formatOnSave": false
	},
	// tell the ESLint plugin to run on save
	"eslint.autoFixOnSave": true,
	// vetur config
	"vetur.format.defaultFormatterOptions": {
		"js-beautify-html": {
			"wrap_attributes": "force-expand-multiline",
		},
		"prettyhtml": {
			"printWidth": 100,
			"singleQuote": false,
			"wrapAttributes": false,
			"sortAttributes": false
		},
		"prettier": {
			"singleQuote": true,
			"trailingComma": "none"
		}
	}
  ```
  ## Acknowledgement

  Credit Wes Bos https://github.com/wesbos/eslint-config-wesbos
