# pinia-tasks

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

# Vue3PinaTasks

# json server の使い方

- "data"ディレクトリをルート直下に作る
- data dir の中に"db.json"ファイルを作成
- "npm install -g json-server"で json-server をインストール
- "son-server -w ./data/db.json"で json-server の参照元を指定
- 上記を実行するとエンドポイントが作成されるのでそれを非同期処理に使える
