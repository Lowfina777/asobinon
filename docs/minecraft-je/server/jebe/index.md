---
slug: /minecraft-je/server/jebe/
title: 【Minecraft】JEとBE両方で入れるサーバーを立てる手順
sidebar_label: 目次
sidebar_position: 0
---

# JEとBE両方で入れるサーバーを立てる手順

このチュートリアルでは、マインクラフトのJEとBEのどちらでも入れるサーバーを立てる方法を解説します。具体的には、UbuntuでPaperサーバーを立てて、Gayser+FloodgateでBEと繋ぎます。

## 前提条件

サーバーを立てる前に、以下のことを確認してください。

- [ ] VPSはお金がかかることを理解している
- [ ] ターミナル・コマンドプロンプトをいじったことがある
- [ ] エラーの英語から原因を推察できる
- [ ] 何かしらのパスワードマネージャーを使っている
- [ ] 基本的な英語が読める

**一つでも欠けると苦戦する**と思います。それぐらい手間のかかる作業をします。

:::warning
Windowsの場合、文中の`control`は`Ctrl`キーで代用できるはずです。
なお、サーバーとほぼ同じコマンドが使えるという意味で**Macを使うことをおすすめします。**
:::

## 事前に用意するもの

### 学生優待GitHub Proアカウント

これを下のTermiusと連携させます。

Proが使えない場合、OSのターミナルでSSH接続してください。

:::info 学生へ
**大学生の方は、無料でGitHub Proを使えます。**
:::

### Termius

[[dl|Termiusのダウンロード]]
|**<https://termius.com/>**

Termiusは、SSHに加えてSFTPもできるクライアントです。ダウンロードしましょう。

同時にTermiusアカウントを作って、**学生認証したGitHubアカウントと紐づけてください。Termiusの有料機能が使えるようになります。**

### Vultrアカウント

[[dl|Vultr]]
|**<https://www.vultr.com/>**

VultrというVPSを借りてサーバーを建てていきます。

![Vultrに入金](https://bn02pap001files.storage.live.com/y4mrbDh222WCVdaNvZQ80lkhWbg0HvLyy4ezfY1_-r0HG2a1qPGj4rYzcQG0UuutyJ50tVjLDPbRT7iZRgXD8kUKt_-bEfHPB9C-EMAe3coquxF4TmdaxuKezMUFjZ4Hc0KBvYueqTXwqPu22gc4U6V_PphWV3IHObEnkMvwc5pFX8f1f6JPwmCD4gMwVJoUuD4?width=660&height=308&cropmode=none)

「Billing」画面を開き、PayPalなどを使って、**10ドルほどクレジットを入金しといてください。**

:::info
次のページでは、サーバーをデプロイします。
:::
