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

Create `.prettierrc` file with the following content:

```json
{
  "semi": true,
  "singleQuote": true,
  "printWidth": 80,
  "trailingComma": "es5",
  "arrowParens": "avoid"
}
```

which can be done as follows:

```bash
cat <<END > .prettierrc
{
  "semi": true,
  "singleQuote": true,
  "printWidth": 80,
  "trailingComma": "es5",
  "arrowParens": "avoid"
}
END
```
