---
slug: /minecraft-je/server/jebe/
title: JEとBE両方で入れるサーバーを立てる手順
sidebar_position: 0
---

このチュートリアルでは、マインクラフトのJEとBEのどちらでも入れるサーバーを立てる方法を解説します。

## 前提条件

サーバーを立てる前に、以下のことを確認してください。

- [] GUIなしで(コマンドで)パソコンをいじったことがあるか?
- [] 何かしらのパスワードマネージャーを使っているか?
- [] 基本的な英語が読めるか?

一つでも欠けると苦戦すると思います。

:::warning
Windowsの場合、文中の`control`は`Ctrl`キーで代用できるはずです。
なお、サーバーとほぼ同じコマンドが使えるという意味で**Macを使うことをおすすめします。**
:::

## 事前に用意するもの

### GitHubアカウント

**学生の方は、GitHub Proを使えます**。これを下のTermiusと連携させます。

### Termiusアカウント

[[dl|Termiusのダウンロード]]
|**<https://termius.com/>**

Termiusは、SSHに加えてSFTPもできるクライアントです。

上記のサイトでTermiusアカウントを作って、**GitHub Proと紐づけてください。Termiusの有料機能が使えるようになります。**

### Vultrアカウント

[[dl|Vultr]]
|**<https://www.vultr.com/>**

VultrというVPSを借りてサーバーを建てていきます。

![Vultrに入金](https://bn02pap001files.storage.live.com/y4mrbDh222WCVdaNvZQ80lkhWbg0HvLyy4ezfY1_-r0HG2a1qPGj4rYzcQG0UuutyJ50tVjLDPbRT7iZRgXD8kUKt_-bEfHPB9C-EMAe3coquxF4TmdaxuKezMUFjZ4Hc0KBvYueqTXwqPu22gc4U6V_PphWV3IHObEnkMvwc5pFX8f1f6JPwmCD4gMwVJoUuD4?width=660&height=308&cropmode=none)

「Billing」画面を開き、PayPalなどを使って、**10ドルほどクレジットを入金しといてください。**

:::info
次のページでは、サーバーをデプロイします。
:::
