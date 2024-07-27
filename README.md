## eslint-nextjs-repo

to run prettier run as

```
npx prettier . --write
```

setup prettier with husky:

1. install prettier

```sh
npm install --save-dev husky lint-staged
```

2. setup husky

```sh
npx husky init
```

3. write to pre-commit file

```sh
node --eval "fs.writeFileSync('.husky/pre-commit','npx lint-staged\n')"
```

4. setup in package.json:

```
{
  "lint-staged": {
    "**/*": "prettier --write --ignore-unknown"
  }
}
```
