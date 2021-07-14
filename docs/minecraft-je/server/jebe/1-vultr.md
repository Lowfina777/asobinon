---
title: ステップ1. サーバーデプロイと接続 | JEとBE両方で入れるサーバーを立てる手順
sidebar_label: ステップ1. サーバーデプロイと接続
---

# ステップ1. サーバーデプロイと接続

## 新しいサーバーをデプロイ

![Deploy New Server](https://bn02pap001files.storage.live.com/y4migEtChZhRl-lCuuqWxUuhOCKkfY4kHdvVbHg_1a0w2ZLGYHDLS5qyl--CiO8cfx6zKHtnz9w2c_Spb3h5uGpJg8ET29VzvzIVZZM6I_Zok-n-aTGigTJ2meKCKmZ4dHixAmzHP9fYd8yItmkjRbvhKc9cJwd0N_2rICh1ZChMgLbvJvw0DMVEFB8qeTLehUw?width=660&height=480&cropmode=none)

Vultrの「Products」-&gt; プラス -&gt; 「Deploy New Server」で新しいサーバーをデプロイします。

![Ubuntu](https://bn02pap001files.storage.live.com/y4mFDLdB0KaZ3-jBAXNStpLKkzYY8Btej20uKMvlSoaPWUxblrLEEfKoOT4rMw1yO253LdhuG__fvlNayzFwGzfPF8eIJoAS-7j6z4RSm7yiSORpkYnVDWzNRYzvEFqJWQyGsCHJJewVNHbsG8zRf1GmbLcJfynk4j1TfpobBxJyQWv2-WwZnjIXB172tb5iHkJ?width=484&height=660&cropmode=none)

以下のものを選びます

|項目|選択肢|
|---|---|
|Choose Server|Cloud Compute|
|Server Location|Tokyo|
|Server Type|Ubuntu (x64)|
|SSD|25GB|

2021年7月14日現在、**この構成で月5ドル**になります。

「Server Hostname」は`mc-paper`、「Label」は`マイクラBEJE`などにしましょう。

:::warning
暗号鍵を本来は設定すべきですが、説明の都合上省略します。
鍵を使ったSSH接続はここでは説明しません。
:::

[[dl|なぜUbuntu?]]
|Java版だけならCentOSで構わないが、**万が一BEのサーバー(BDS)を動かす必要が生じた時のため。**BDSはUbuntuを想定して作られている。

## Termiusで接続

![IPとパス](https://bn02pap001files.storage.live.com/y4mBzqWb9oGNnKLJiEtZybWbR6iCp1R0qFiacqQoNI25eCJIsV_qYcZQ9o7AAjZ51215SWJcBxIVJdRJoXtBO0AxsHc_AXMuIFjU2HcPZAAGCLSJis7329eBP0dI_2_lq82VUkgdiUirch36E4gQs5tFjK2Jy8MUAbERbBGOE9ldAwqeyaiq0NGSIToUOjq9KZF?width=332&height=386&cropmode=none)

サーバーをデプロイしてしばらく経つと、**IP**がわかるようになります。必ずパスワード管理ソフトなどにメモしましょう。

また、**`root`ユーザのパスワード**も必ずパスワード管理ソフトなどに記録してください。

:::info
IPに対して独自ドメイン(なんちゃら.comなど)を設定できます。詳しくは[ステップ6](./6-domain)をご覧ください。
:::

![Termiusで接続](https://bn02pap001files.storage.live.com/y4mar-Qb3mDUlDPVQQ5U9Z5UCV6HBT0Dvyb-__dsBV4eVE0BzAVBF9UDiN0XmfUHiPVuqG-OzsrmOwMg2Tn6ejQo9p19qofuWSyrHVntBGmU2SC-9ro3bPrfh642uzUhhFp87oTasDxK9O2XRE4jpKZkcYTvSSFqcgE2R1eHU3LclnY3lMKVRO7dDqO4ZXaIL9B?width=650&height=300&cropmode=none)

Termiusをインストールしてログインし、「NEW HOST」をクリックしてください。

以下のように設定して保存してください。

|項目|選択肢|
|---|---|
|Label|`マイクラサーバー(root)`|
|Adress|さっきのIP|
|Username|`root`|
|Password|さっきのroot用パス|

「SAVE」を押して保存し、ダブルクリックします。接続できたでしょうか。

:::info
信頼するホストに追加するか聞かれた場合は、`Yes`を選んでください。
:::

![root接続成功](https://bn02pap001files.storage.live.com/y4mShOyb1dZmiDvKJ_qtlJZoIzxdRSkJvKjZok4M6wwXGADdKqt6xoPJymMUBo0cBOoFwIPPfrgrbSymIOzo4duAf4CPahJEShClKR_oIB7ExH_0QzZmwdBMVrXLhoE75lbecfdIIP80NLflXgWAJvwBIQ0ZHa3ULaeJAUyDCa8zqtocdDhQmqOW6aCRkkW8dSW?width=256&height=99&cropmode=none)

IPとパスが正しければこんな画面が出るはずです。

:::info
次のページで、ユーザの作成をします。
:::
