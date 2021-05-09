---
sidebar_position: 3
---

# Cloud functionsのセットアップ

## レポジトリ上での作業

```sh
firebase init
cd ./functions
```

からの

```sh
firebase functions:config:set twitter.bearer="キー"
firebase functions:config:set twitter.secret="キー"
firebase functions:config:set contentful.public="キー"
firebase functions:config:set contentful.space="キー"
firebase functions:config:set contentful.limit="キー"
firebase functions:config:set contentful.manage="キー"
firebase functions:config:set contentful.preview="キー"
firebase functions:config:set contentful.maxage="キー"
firebase functions:config:set contentful.auth="キー"
```

でキーをセット。

### データインポート

`./firestore_import/firestore_sync.sh` を自分のバケットに書き換えて、

```sh
firebase functions:config:get > .runtimeconfig.json
sh ./firestore_import/firestore_sync.sh
```

を実行してください。Firestore のデータがローカルにコピーされます。

## emu

```sh
npm run dev
```

## deploy

```sh
npm run deploy
```
