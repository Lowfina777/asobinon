---
title: ステップ2. サーバー用ユーザの作成
---

## サーバー用ユーザの作成

rootでマイクラサーバーをいじるのは危険なので、`minecraft`ユーザを作ります。

:::warning
まずパスワード管理ソフトなどで、`minecraft`ユーザ用のパスワードをrootと別に作ってください。
:::

```bash
adduser minecraft
# ここでminecraftユーザ用のパスワードを設定する
# パスワード以外は全部Enterで飛ばしていい
gpasswd -a minecraft sudo
```

ユーザーを作れたら、<kbd>control</kbd>+<kbd>D</kbd>でサーバーからログアウトしてください。

[[dl|豆知識]]
|SSHクライアントでは、<kbd>control</kbd>+<kbd>D</kbd>でサーバーからログアウトする。

## Termiusでマイクラ用ホストを追加

![ホスト複製](https://bn02pap001files.storage.live.com/y4mqwiKvPoH5q4kvf9NmB53oXuPpUa9XYw5_O7ooAJmId--ZUgwxlgqcm4XKj075jsZHZWWpYcnoEBZcfi9InjLfi1x-SXr_His47QSPdr2SdHdDNiA3jgwp-l-6rd4KheXSA6rX8qz-XUx77Fq-Fsca6wPbsiJwn3AV41y4bEPqG2o4NzUsSATgek-iIy9PX0N?width=256&height=188&cropmode=none)

先ほどのroot用ホストを「Duplicate(複製)」します。

![Edit](https://bn02pap001files.storage.live.com/y4msjaYiL9NzoOE6XHppxRNV0IukD-Sw54qojh33Te9u4E-v5U0OAy5Ei1cvx6R71wSKGJHiZ5slHLTY4O0S3ooLOTdFDG0rWOVOjeOIjHyUw4q8pNzvONMQC40BaUDfJ2_erjj6NUNHSNnFB_jMKIHOc5rR3u8h4sOsUxswhaot0bnJxyLiKEfsWpExCYko_Hk?width=256&height=168&cropmode=none)

複製されたホストを「Edit(編集)」します。

![ラベル変更](https://bn02pap001files.storage.live.com/y4mP1Zy5znrcx98vRHOkHjMtRYL3NMp8As5ylIMppveIWdUa08o6ghe5c3Az1ShT5h1lfwS5NtbrD7vjFpMe950IxY1fGH1uaL8UUHWgvOvATrzeoW-0512LLra0L3oWOfzsLRRxB8kUAz2D96zZKaFEjjSdvnInHWNPeRasGdDaodBLIS9JKWkGhx5vju8MaiM?width=256&height=96&cropmode=none)

「Label」を`マイクラサーバー(minecraft)`に変えます。

![ユーザ変更](https://bn02pap001files.storage.live.com/y4m7vRaCih75d9fZw-0bK1ILalPVfqQzkd-v75a0bxWgJDYn6jxLbrYx7IIwtsW7PZTGJ_OlIT0r3u9h4eGY-BXruIRmF20wQGgLeKq1XFGUlxn0HVKV0VYZ3z63P1ABMZMwArviazViOoDH_EjIVP6C2QjMSVFNa63aVCPruqPaEyrXBaXdQoLRuXGhjsFl6eD?width=256&height=126&cropmode=none)

ユーザー名を`minecraft`に変え、**パスワードも先ほど作った`minecraft`ユーザ用に変えてください。**

![できた](https://bn02pap001files.storage.live.com/y4mAs0FhT2rGZOw_KC6OKy_h8eICFfdcNZ6WC9cRmiu552yjdO1ob6vxEdAH0bYiyzR8hjcNVKQj2JG9j-kGSRUKuiy0MqFvrBBGiq0gckKIg58BYZ-fp5y7Mc1Ckl6lvHR2wt8K_nmSyD9jpIbFRFre48oe5t5sxae0mLOcyk3xxYKqPbmIo9AExXN6nKwbow6?width=256&height=84&cropmode=none)

「SAVE」してダブルクリックし、`minecraft@サーバー名`と出たら成功です。

:::info
次のページで、paperをインストールします。
:::
