---
title: メニューや検索ボタンが使えなかった不具合を修正しました
author: sasigume
author_title: 管理人
author_url: https://twitter.com/sasigume
author_image_url: https://pbs.twimg.com/profile_images/1399002027565350914/kv4sWMwT_400x400.jpg
tags: ["全体的なこと"]
---

当サイトにて、メニューバーや検索欄が一切使えなくなる不具合が、少なくとも6月下旬には把握されていました。3週間近く放置してしまいましたが、この度修正したことをご報告します。修正が遅れて申し訳ありませんでした。

<!--truncate-->

## 今回影響を受けた部分

サイト左側のメニューが展開できなくなったほか、ページの読み込みもその都度読み込む状態になってしまい、サイト全体のユーザビリティが最悪になりました。

## 問題のあった箇所

コードを埋め込むプラグイン(`@saucelabs/theme-github-codeblock`)に必要なBabelプラグイン(`@babel/plugin-transform-modules-commonjs`)を、最新の環境では不要なのにも拘らず、`babel.config.js`で指定していました。

該当するプラグインを削除すれば動いたと思うのですが、まさか2021年7月12日現在のレポジトリの説明と違ってなくても動くと思わず、原因の発見に時間がかかりました。
