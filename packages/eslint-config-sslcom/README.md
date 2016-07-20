# eslint-config-sslcom

This package provides SSL.com's .eslintrc as an extensible shared config.

## Usage

We export three ESLint configurations for your usage.

### eslint-config-sslcom

Our default export contains all of our ESLint rules, including ECMAScript 6+ and React. It requires `eslint`, `eslint-plugin-import`, `eslint-plugin-react`, and `eslint-plugin-jsx-a11y`.

1. `PKG=eslint-config-sslcom npm info "$PKG" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG"` (which produces and runs a command like `npm install --save-dev eslint-config-sslcom eslint@^2.9.0 eslint-plugin-jsx-a11y@^1.2.0 eslint-plugin-import@^1.7.0 eslint-plugin-react@^5.0.1` but with whatever the proper version numbers are)
2. add `"extends": "sslcom"` to your .eslintrc

### eslint-config-sslcom/base

This entry point is deprecated. See [eslint-config-sslcom-base](https://npmjs.com/eslint-config-sslcom-base).

### eslint-config-sslcom/legacy

This entry point is deprecated. See [eslint-config-sslcom-base](https://npmjs.com/eslint-config-sslcom-base).

See [SSL.com's Javascript styleguide](https://github.com/sslcom/javascript) and
the [ESlint config docs](http://eslint.org/docs/user-guide/configuring#extending-configuration-files)
for more information.

## Improving this config

Consider adding test cases if you're making complicated rules changes, like anything involving regexes. Perhaps in a distant future, we could use literate programming to structure our README as test cases for our .eslintrc?

You can run tests with `npm test`.

You can make sure this module lints with itself using `npm run lint`.