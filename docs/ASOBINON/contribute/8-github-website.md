---
title: ステップ8. GitHubサイト上で編集する
sidebar_label: GitHubサイト上で編集
---


## 「この記事を編集」を押す

下か上にボタンがあるはずです。

## GitHubアカウントを作る

ない場合は作ってください。無料です。

:::note
学生なら無料で`PRO`アカウントにアップグレードできます。
:::

## 編集する

![](https://bn02pap001files.storage.live.com/y4mCeIn7IROd2ciCUVfD3UFi7vfo0E4xpV-daeavVHa_pK5jsL3XxWczUXRypi1bZOcDwZOFYN_YCLYNek8Up2FciKcdrZkossBLPSUqUT7mBv7NgRzgCvltwNFkMThCvIRGTTeJWn8Qt4N9EaFzD75V4YtjzGOIy01lzu18hBwDpeJJfYOLEf6gUcMpbYH2tO6?width=660&height=157&cropmode=none)

まず**「Fork this repository」**ボタンを押してください。

## コミットする

![](https://bn02pap001files.storage.live.com/y4mDauBJmFwWx9MT00-rkUZAIcIpVcDxaVbIsH9p_8dyRRvZ7PWmSX5ZMlJe_T6GLArhR95RHZYucktCeK1wMeayANAIz61xzsnUxSn6SOzNgdRecObLT3nHMaJsXsfr90pHSHD7MIYETnesyMttXc26iyFa8R24ZOOoSrSVd2Vh99CgQUMluhyl-dI9u7avv4L?width=660&height=522&cropmode=none)

編集して、**何を変えたかを「コミットメッセージ」に書きます**。

そして**「Propose changes」**を押してください。これで**自分のフォークにコミット**ができました。

## プルリクエストする

自分のフォークを、**本物に統合(マージ)**させます。

![](https://bn02pap001files.storage.live.com/y4mC2UlfA2HSETY7Gps_o6B6CHBtC7YHHQUUFaDZtAEd6O1AarKF57Rx4OU2q8ct_vxTl8UksShJWT7aB6XSfL-N_4COBe6km4YFUjZ_O1gtuZ1nZWaQ8RRN8dgfoYUH8SHYmQdf2jdJnWhxP1SlvYgVOWtW3vMwMko8XxaebgWeucGze_GbjeRLUqxVCbhA8o0?width=660&height=264&cropmode=none)

この画面が出たら、右下の「Create Pull Request」を押してください。

![](https://bn02pap001files.storage.live.com/y4mZNRO1gpbjAGhW8R_MZDXktHVE0zIEnM3Hks5IzIf2xvh2z8b1klohZh68PYKhwY7_LXLxv-4Adw4b8SVrNNBFco91pYXuZ5G_GCfVLqV1j-MnWDd24p6wu50iKx714nIPkIsGEgXFh_Ik-ZB-suabR-ntA56fNvnMR1QWnmkF0Z0dz5mDd9shppWDc7V5Lfn?width=660&height=483&cropmode=none)

さっきも何を変えたか書いたと思いますが、ここではその**概要**を書きます。(複数のコミットをまとめてリクエストできるので)

「Create Pull Request」を押せば、ビルドが始まり、成功すれば反映されます。

:::warning
成功した後も、更新には三分ほど時間がかかります。
なぜなら、**最初のビルドは「プルリクエストのビルド」**だからです。
:::

## ビルドに失敗した場合

![](https://bn02pap001files.storage.live.com/y4mDk5vDlnU8A3AL5xAO8RjB9qkW2hnGJ-zBMmgFNernv2bhKmU1cbD3sJLIL0xTExYnHIziM0JFAXEvJGw8BuknTQSEgZ2FnKKI8i1_q6O4xde-GGJ0QniGBM_im5AGCTAftoSEnucu0ssGqFOlS3KMp6wkTdT-vaH1mWb1PvZ3OEs-1RhBMizDu8Br5nPl-Sr?width=660&height=286&cropmode=none)

`Some checks were not successful`と出たら、「ビルドに失敗した」ということです。

JSXが間違っているなどの理由が考えられるので、編集内容を見直してください。

もちろん記事以外の`js`ファイルなどを不用意にいじっても失敗します。
