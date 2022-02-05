# my-vue-linter-setups

## 前提

Vue.js(v3)に合わせた設定の記録

## VSCode の設定

-> "Vue VSCode Snippets", "Vetur"を無効にしておく

## create project

```
$ yarn create vite $PROJECT_NAME
✔ Select a framework: › vue
✔ Select a variant: › vue-ts

$ cd $PROJECT_NAME
$ yarn
```

## eslint

### Vue, TypeScript 対応

参考: https://zenn.dev/chida/articles/c0bd3ad56ed06b

```
$ yarn add -D eslint eslint-plugin-vue @vue/eslint-config-typescript @typescript-eslint/parser @typescript-eslint/eslint-plugin
```

### a11y 対応

参考: https://zenn.dev/azukiazusa/articles/vue-a11y-testing

```
$ yarn add -D eslint-plugin-vue-a11y
```

### 設定

```
# eslintrc の内容はリポジトリ参照
$ touch .eslintrc.yml
```

```
# package.json
"scripts": {
...
"lint": "eslint --fix src/_.{ts,vue} && eslint --fix src/\*\*/_.{ts,vue}",
},
```

## prettier

参考: https://zenn.dev/chida/articles/c0bd3ad56ed06b

```
$ yarn add -D prettier @vue/eslint-config-prettier
$ touch .prettierrc.yml
```
