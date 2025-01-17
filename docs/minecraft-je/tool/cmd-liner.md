---
title: どんな見辛いコマンドも、一瞬で綺麗に。コマンド整形ツール「CmdLiner」の紹介
---

[![CmdLiner](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208132830.png)](#2/d/2d19a90c.png "CmdLiner")  
カスタマイズしたゾンビの召喚など、長いコマンドをフォーラムで見かけたあなた。  
**自分好みにコマンドを弄ろうと思っても、どこを編集したらいいのか分からない…  
コマンドのどこからどこまでがカッコなのか分からない!って経験ありませんか?**  
そんな時は、[Argon氏](https://twitter.com/Argon_MC)制作の**コマンド整形ツール「CmdLiner」**を使いましょう。

## 目次

*   [こんな経験ありませんか?](#ouch)
*   [コマンド整形ツール「CmdLiner」のダウンロード](#download)
*   [コマンドを整形/圧縮でき、細かい設定も可能](#howto-line)

## こんな経験ありませんか?

[![長いコマンドが投稿されてる](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208142302.jpg)](#6/4/64c0d43e.jpg "長いコマンドが投稿されてる")

某フォーラムにて、こんな投稿を見かけたあなた。見るからに**ゾンビをスポーンさせるコマンド**ですが、**色々カスタマイズされている事が分かります。**面白そうと思ったあなたはコマンドを使ってみます。

[![ありきたり](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208125834.png)](#0/e/0ec6ca40.png "ありきたり")

うーん、馬に乗ったゾンビ… ありきたりな感じですね。  
「ゾンビのHPを増やそう」「装備を変えよう」と考えたあなた。コマンドを弄ろうとしますが…

/summon Zombie ~ ~1 ~ {CustomName:”つよいぞんび”,CustomNameVisible:1,Equipment:\[{[id:diamond\_sword](http://blog.hatena.ne.jp/diamond_sword/),Count:1,tag:{display:{Name:つよいけん,Lore:\[“つよいぞ”\]},ench:\[{id:16,lvl:5},{id:34,lvl:5}\]}},{},{},{},{}\],DropChances:\[1.0F,0.085F,0.085F,0.085F,0.085F\],Attributes:\[{Name:generic.movementSpeed,Base:1.5},{Name:generic.attackDamage,Base:100}\],Riding:{id:”EntityHorse”,CustomName:”お馬さん”,CustomNameVisible:1,Type:0,SaddleItem:{[id:saddle](http://blog.hatena.ne.jp/saddle/)},Variant:0,Equipment:\[{[id:diamond](http://blog.hatena.ne.jp/diamond/),Count:1,tag:{display:{Name:だいや}}},{},{},{},{}\],DropChances:\[1.0F,0.085F,0.085F,0.085F,0.085F\],Attributes:\[{Name:generic.movementSpeed,Base:1.5},{Name:horse.jumpStrength,Base:100}\],HealF:100}}

こんなにズラーっと不格好に文字列が並んでいるので、**どこに手を付ければいいのかさっぱり分かりません。**下手に弄ったらコマンドが駄目になりそうですもんね…

この複雑なコマンドを、**私が一瞬で綺麗にして差し上げましょう。**

/summon Zombie ~ ~1 ~ {
CustomName:"つよいぞんび",
CustomNameVisible:1,
Equipment:\[
{
[id:diamond\_sword](http://blog.hatena.ne.jp/diamond_sword/),
Count:1,
tag:{
display:{
Name:つよいけん,
Lore:\[
つよいぞ
\]
},
ench:\[
{
id:16,
lvl:5
},
{
id:34,
lvl:5
}
\]
}
},
{
},
{
},
{
},
{
}
\],
DropChances:\[
1.0F,
0.085F,
0.085F,
0.085F,
0.085F
\],
Attributes:\[
{
Name:generic.movementSpeed,
Base:1.5
},
{
Name:generic.attackDamage,
Base:100
}
\],
Riding:{
id:"EntityHorse",
CustomName:"お馬さん",
CustomNameVisible:1,
Type:0,
SaddleItem:{
[id:saddle](http://blog.hatena.ne.jp/saddle/)
},
Variant:0,
Equipment:\[
{
[id:diamond](http://blog.hatena.ne.jp/diamond/),
Count:1,
tag:{
display:{
Name:だいや
}
}
},
{
},
{
},
{
},
{
}
\],
DropChances:\[
1.0F,
0.085F,
0.085F,
0.085F,
0.085F
\],
Attributes:\[
{
Name:generic.movementSpeed,
Base:1.5
},
{
Name:horse.jumpStrength,
Base:100
}
\],
HealF:100
}
}

どうです? 綺麗でしょ。  
これなら、**どこからどこまでがカッコで括られているのか一目瞭然ですね。**  
ですが私は人間。こんなに綺麗には書けません。**とあるツール**の手を借りました。

## コマンド整形ツール「CmdLiner」のダウンロード

コマンド整形ツール「CmdLiner」のダウンロード

[http://mcargon.web.fc2.com/minecraft/cmdliner.html](http://mcargon.web.fc2.com/minecraft/cmdliner.html "コマンド整形ツール「CmdLiner」のダウンロード")

**Twitterでコマンド関連の投稿をしておられる[Argonさん](https://twitter.com/Argon_MC)**の制作です。安心ですね。

[![2015-7-3_22-43-12-min](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208175610.jpg)](#f/4/f47c8867.jpg "2015-7-3_22-43-12-min")

ダウンロードしたzipを展開し、中の_「CmdLiner.jar」_をJava SEで実行して下さい。

## コマンドを整形/圧縮でき、細かい設定も可能

![貼り付けて、整形。](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208133340.jpg)  
真っ白なフィールドに、読みづらいコマンドをダァッーっと流し込みましょう。  
そして**「変換」→「Raw→Lined」を押す**と、一瞬でコマンドが整形されます。

![文字も綺麗..?](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208160131.jpg)  
コマンド内の「{}」「,」などで改行し、タブ(大きな空白)を挿入することで綺麗にしているんですね。  
ところで、**私の画面では文字がザラザラしてませんね。**どうやってフォントを変えたんでしょうか。

![フォントなどを設定](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208161323.jpg)  
答えは簡単。**同梱されている「cmdliner.properties」を編集**すればいいだけです。  
設定ファイルは日本語で分かりやすく書かれているので、特に解説する必要はないでしょう。

![圧縮もできる。](https://cdn-ak.f.st-hatena.com/images/fotolife/s/sasigume/20210208/20210208144913.jpg)

このツール、コマンドを整形するだけでなく、**余計な改行を消して「圧縮」もできる**んです。  
フォーラムや、pastebin.comなどのサイトにアップする時に便利ですね。
