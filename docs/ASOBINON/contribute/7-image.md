---
title: ステップ7. 画像アップ
sidebar_label: 画像アップ
---

申し訳ありませんが、ストレージの費用の関係から、「アソビノンのサーバーに画像をアップロードする」機能は用意しておりません。

技術的には可能ですので、以前は動かしていたんですが、ストレージに対して課金が発生するため、諦めました。

## GitHubにペーストして画像をアップする

:::info 忘れていました
このアップ方法を完全に忘れていました。GitHubすごい！
:::

まずは「この記事を編集」を押してGitHubの編集ページを開きます。

それから、**アップしたい画像を、クリップボードにコピーしてください。**

|OS|コピー方法|
|---|---|
|Windows (10以上)|<kbd>Win</kbd>+<kbd>Shift</kbd>+<kbd>S</kbd>|
|macOS|<kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>4</kbd>|

![image](https://user-images.githubusercontent.com/74000913/125961056-e288f819-f2a8-43c6-8ff7-0931404ab064.png)

**GitHubにペーストするだけで、自動でアップロードされます。** ただし10MBまでです。

![image](https://user-images.githubusercontent.com/74000913/125961033-d093f411-ea27-479b-a9cb-dd38e5480680.png)

例えば▲この画像はクリップボードからペーストしました。

## OneDriveを使った画像アップ (非推奨)

:::warning
アソビノン運営は、OneDrive上のトラブルについて責任はおいかねます。ご了承ください。
:::

### 1. OneDriveにアップロード

パソコンの場合は **OneDriveフォルダ** に画像を入れてください。

iOS/iPadOS/AndroidではOneDriveアプリを入れておけば、写真アプリの共有画面から、OneDriveを選んでアップロードできます。

:::caution
OneDrive上でファイルを消すと、サイト上でも見れなくなる** ので、分かりやすいフォルダ名をつけましょう。
:::

### 2. OneDriveのサイトで埋め込みURLを取得

次に、埋め込み用のURL (**共有リンクではない**) を取得する必要があります。

- パソコンの場合、ファイルを右クリックして「オンラインで表示」を選んでください。
- iOS/iPadOS/Androidでは、WebブラウザでOneDriveのサイトを開いてください。

画像を選んで、「埋め込み」をクリックしてください。

![](https://bn02pap001files.storage.live.com/y4mg9v8M3JU41qgEnk6iGjxt8eGJabsJeD35iDxVDoSZ19abESoxhZ5NnUq6-cktmaNoMqbyfG3SCbDcGiGHm9JmCFjtVEA_bE3sUCM_k6Qx2sm19aolZXv4vhj9it2Oyh7TTDxg_v9BWDpETHr_5iwdDzJ-9cpsB8UPYh_W4q1kd7KIOxDubRfKYg-iztAEmNI?width=580&height=660&cropmode=none)

「埋め込み用コードを生成」の下の**「生成」**を押してください。

![](https://bn02pap001files.storage.live.com/y4m3Og89gKVSSwhi-kHDMVWnffTC1y5bKdyWW7dcCZN0YV49r5RMQ-iL7yEeOLkFFzY8uR2rGGCtizT-fcf2cq9gUVWAz887Bv60PAyUnFRbL849DEtiVmF9zgYvD5dR92GCa0rnOXRPReU3iM31Bhi4VySoNqo_Mvy4D88jxQDkwpAAJwHsurqCafYZa6q2vQs?width=625&height=660&cropmode=none)

そのままでは大きすぎるので、サイズを**中**にしてください。下に画像のURLが表示されます。

### 3. 画像を埋め込む

```md
![説明](URL)
```

記事編集画面で、このように書けば、画像が表示されるはずです。

:::warning HTMLは使わないでください
HTMLのimgタグは使わないでください。DocusaurusはMDXという規格でページを生成するので、閉じタグを忘れたりといった理由で更新に失敗しやすくなります。
:::
