# 💻 Getting Started

## 事前にインストールするソフトウェア

- Node 18.15.0 (←現時点での[LTS版](https://nodejs.org/ja)を記載すること)

### インストール方法

- 推奨：nvm経由でインストール([リンク](https://github.com/nvm-sh/nvm))
- 非推奨：Node.jsのWebページからインストール([リンク](https://nodejs.org/ja))

## ソースコードのクローン

以下のコマンドを入力して任意のディレクトリに本レポジトリをcloneしてください。

```shell
$ git clone https://github.com/*****.git
```

## アプリケーションの立ち上げ

- 本レポジトリのクローンが完了したら以下のコマンドを入力し`http://localhost:3000`でアプリケーションが立ち上がることを確認してください。

```shell
$ cd [リポジトリ名]
$ cp .env.example .env
$ npm install
$ npm run dev
```

- アプリケーションの動作が重いと思ったら、以下のコマンドを入力してもOKです！
- 以下のコマンドの場合はCodeの修正が即座にアプリには反映されないので、1度アプリケーションを止めてからもう1度以下のコマンドを入力してください。

```shell
$ npm run build
$ npm run start
```
