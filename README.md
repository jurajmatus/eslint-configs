# Usage

## ESLint

Install the config of your choice, eslint and prettier:

```bash
yarn add -D eslint prettier
# one of
yarn add -D https://gitpkg.now.sh/jurajmatus/eslint-configs/packages/eslint-config-ts-node-strict
```

Add this to `.eslintrc.json`:

```diff
{
-  "extends": [],
+  "extends": ["ts-node-strict"],
}
```

which can be done with `jq`:

```bash
(cat .eslintrc.json || echo '{}') | jq '.extends += ["ts-node-strict"]'
```

## Prettier

Install the config:

```bash
yarn add -D https://gitpkg.now.sh/jurajmatus/eslint-configs/packages/prettier-common
```

Create `prettier.config.js`:

```js
module.exports = {
  ...require('prettier-common'),
};
```

which can be done as follows:

```bash
cat <<END > prettier.config.js
module.exports = {
  ...require('prettier-common'),
};
END
```
