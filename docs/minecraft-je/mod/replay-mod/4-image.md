---
title: ReplayMod完全ガイド Part4 リプレイの中に画像(文字)を貼り付ける
---

[![ReplayMod画像貼り付け](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208135429.png)](#4/a/4a71d7d3.png "ReplayMod画像貼り付け")

**リプレイを保存し、カメラの動きを設定、動画として書き出せる。**革命的なカメラMOD**「ReplayMod」**。今回は解説記事第三弾、**「リプレイ内に画像(文字)を貼り付ける」方法を解説します。最近ゲームのトレイラーなどで流行りのスタイルですね。**サーバーや配布ワールドの紹介動画づくりに、是非ご活用下さい。  
(サムネ内のロゴは作者さんのものをお借りしました。撮影ワールドは[AcrossTheTime](/minecraft-je/world/acrossthetime/)」です)

※この記事は**2015年11月15日現在**最新の**ReplayMod「v1.0.6」**を使っています。今後のバージョンアップによって、作業の手順が変更になる場合もありますのでご注意下さい。

## ReplayModの基本的な使い方、カメラの動きの設定はpart1へ

[![革新的なカメラMOD「ReplayMod」](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208151046.png)](#9/0/90d17ba6.png "革新的なカメラMOD「ReplayMod」")

リプレイを録画し、**後から自由に鑑賞**したり、**カメラの動きを設定**して動画を作ったり… 革新的なカメラMOD、「ReplayMod」。**動画制作に便利な様々な機能を解説していくシリーズの、今回は3回目**です。

**第一回、それと第二回をお読みになった前提で書いています。**ReplayModでのリプレイの閲覧やカメラの動かし方、動画として書き出す手順については上記part1とpart2をお読み下さい。

## 「リプレイ/動画の中に画像を貼り付ける」とはどんな機能?

[![最近のゲームのトレイラーで流行りのアレ](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208133831.jpg)](#3/c/3c0555cb.jpg "最近のゲームのトレイラーで流行りのアレ")

突然ですが、[最近のゲームのトレイラー](http://www.youtube.com/watch?v=vIg5dAeudvQ)でこんな文字を見かけませんか? **文字列がゲーム内に設置してあるかのように写っている、最近流行り(?)の編集スタイルです。**このクールな編集手法を、配布ワールドやサーバー紹介、MOD紹介など、**あなたの作っているマイクラ動画でも使ってみませんか?**

[![こんな風に貼り付けられます](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208132928.png)](#2/d/2dc008a6.png "こんな風に貼り付けられます")

実際に画像を貼り付けるとこんな感じ。**▲では画像編集ソフトで文字を書いて画像にし、ReplayModで読み込んでいます**が、もちろん通常のカラフルな画像も使えます。これだけでトレンディな動画になりそうですね。

## ReplayModで、好きな画像をPCから読み込む手順

それでは、**実際に「ReplayMod」のリプレイ内に好きな画像を読みこませる手順**を解説します。ここでは「ReplayMod v1.0.6」を使っていますが、今後の更新で操作が変更になる場合もあるのでご了承下さい。

[![背景を透明にした画像を作成しよう](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208154324.jpg)](#a/f/afe546c2.jpg "背景を透明にした画像を作成しよう")

まずは貼り付ける画像がないことには始まりません。**ペイントではなく「GIMP」「Photoshop」などの高機能な編集ソフトを使えば、背景を透明にした画像が作れます。**ちなみに、▲で使っているマイクラ風フォントは[こちらの記事](/44816309/)で紹介したものです。

[![Gキーを押してAssetManagerを開く](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208175022.png)](#e/e/ee7f072e.png "Gキーを押してAssetManagerを開く")

次に、ReplayModの**リプレイ閲覧画面でGキーを押しましょう。**すると「アセットマネージャー」の画面が出てきますから**「Add」をクリック**します。

[![先ほど作った画像を選択する](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208131217.jpg)](#1/b/1ba7f861.jpg "先ほど作った画像を選択する")

するとファイルを選択するダイアログが出てきます。**(出てこない場合は、マイクラの起動を何回もやり直すしかありません…)** **先程作った画像や、リプレイ内に貼り付けたい好きな画像を選択しましょう。**

[![画像が追加されたのを確認しよう](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208174813.png)](#e/c/ecec7b99.png "画像が追加されたのを確認しよう")

選択した画像が「アセットマネージャー」の画面に表示されましたね。やっぱり**画像を変えたい場合は「Change Asset File」**を押して下さい。リプレイ内に**画像を貼ってしまった後に変更する場合に便利な機能**です。

## 画像をリプレイ内に貼り付けて、大きさや向きを設定しよう

ただ画像を読み込ませただけじゃ何もできません。**「オブジェクトマネージャー」という画面で画像を貼り付けて、位置や大きさ、向きなどを設定する必要があります。**さらに、設定次第で**「だんだん大きくなる」「途中で向きが変わる」など、画像に動きを付けることも可能です。**

[![Fキーでオブジェクトマネージャーを開こう](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208164728.png)](#e/5/e5a6c03b.png "Fキーでオブジェクトマネージャーを開こう")

Fキーを押して「オブジェクトマネージャー」という画面を開き、**「Add」をクリック**しましょう。

[![オブジェクト名を決めて画像を選択](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208151844.png)](#9/8/98e2b9ce.png "オブジェクト名を決めて画像を選択")

すると新しい「オブジェクト」が追加されます。**「Asset File:」欄で画像を選択**し、適当なオブジェクト名を付けておきましょう。

[![画像の位置を設定しよう](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208180705.png)](#f/d/fde9cc63.png "画像の位置を設定しよう")

画像の位置が気に入らない場合は、**「Position」の値を変更**しましょう。F3で座標を確認して入力すれば簡単です。v1.0.6現在、**入力欄の扱いが難しいです**が←→キーを活用してなんとか入力しましょう。

[![画像の向きを設定しよう](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208152211.png)](#9/c/9c4b3302.png "画像の向きを設定しよう")

**画像の向きを変更する場合は「Orientation」の値を編集します。**Yaw、Pitch、Rollって奴ですね。とにかく**横方向に回したいなら左**、**右に回転させるなら真ん中**、**縦に回転させるなら右**の数字を上下させます。

[![設定が反映されないならここを見なおそう](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208134251.png)](#4/0/407d69d2.png "設定が反映されないならここを見なおそう")

ちゃんと値を入力したのに、反映されない…変な動きをしてしまう… そんな時は、**オブジェクトマネージャーで余計な「キーフレーム」を削除しましょう。****実は設定するタイミングによって、勝手に「キーフレーム」が作成されちゃって意図しない動きになってしまう事がある**んです…

[![キーフレームを使って画像をアニメーションさせる](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208133246.png)](#3/5/35d3dcff.png "キーフレームを使って画像をアニメーションさせる")

「キーフレーム」は、**うまく使えば画像をアニメーションさせられます。**

1.  アニメーションさせたいタイミングまで、**オブジェクトマネージャーの黄色い線を動かす。**
2.  画面左のボタンを押して、**設定したい項目(位置や向きなど)のキーフレームを追加する。**
3.  **そのタイミングの数値を入力する。**設定項目ごとにキーフレームを作る必要がある。

[![上手に画像を見せよう](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208152816.png)](#a/1/a1b1205a.png "上手に画像を見せよう")

Part1で解説したカメラの動きの設定と合わせて、より効果的に画像(文字)を見せてみましょう。**ダイナミックな視点移動と組み合わせるとクールですよ。**完成したらPart2を参考に**動画に書き出すこともできます**ね。

:::info
これでがおず編は終了です! [Part5 スクショ編](./screenshot/)に進みましょう。
:::