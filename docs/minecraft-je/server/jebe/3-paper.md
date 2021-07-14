---
title: ステップ3. paperのインストール | JEとBE両方で入れるサーバーを立てる手順
sidebar_label: ステップ3. paperのインストール
---

# ステップ3. paperのインストール

Paperは、Spigotプラグインを入れられる軽量マイクラサーバーで、現在幅広いサーバーで使われています。
## SFTPで接続しよう

Termiusの「SFTP」を開いてください。

左にパソコンのファイルが出るので、右側のホスト選択で「マイクラサーバー(minecraft)」を選んでください。

:::warning
`root`ユーザでSFTPを使わないでください。事故ります。
:::

おそらく`/home/minecraft/`ディレクトリが出ます。

## paper導入
### paperのダウンロード

[[dl|PaperMCのダウンロード]]
|<https://papermc.io/downloads#Paper-1.16>
### serverディレクトリを作る

```bash
mkdir server
```
## paperを入れてリネーム

`server`フォルダにpaperのjarファイルを入れ、

```bash
cd server

# .XX.X-XXXXXはTabキーで補完してください
mv paper-1.XX.X-XXXXX.jar paper.jar

# 外フォルダに出る
cd ../
```

で`paper.jar`にリネームします。

## スクリプト準備

Vimを使います。

[[dl | Vimの使い方]]
| |||
| |---|---|
| |<kbd>I</kbd>|編集(INSERT)モードに|
| |<kbd>Esc</kbd>|編集終わり|
| |`:wq`|保存して終了|
| 編集(INSERT)モードで`:wq`って打たないでね！必ず<kbd>Esc</kbd>で編集を終わろう。
|

### 起動スクリプトを作る

```bash
vi start.sh
```

#### `start.sh`

```bash
#!/bin/bash

cd $HOME/server

screen -md -S minecraft java -XX:+UseBiasedLocking -XX:+DisableExplicitGC -XX:+UseTLAB -Xms2G -Xmx4G -XX:TargetSurvivorRatio=90 -XX:SurvivorRatio=8 -XX:MaxTenuringThreshold=4 -XX:-UseParallelGC -XX:ParallelGCThreads=2 -XX:ConcGCThreads=2 -jar paper.jar nogui

```

以上を<kbd>Cmd</kbd>+<kbd>V</kbd>でペーストして`:wq`。

### 再起動スクリプトを作る

```bash
vi restart.sh
```

#### `restart.sh`

```bash
#!/bin/bash

WAIT=15
STARTSCRIPT=$HOME/start.sh
SCREEN_NAME='minecraft'

screen -p 0 -S ${SCREEN_NAME} -X eval 'stuff "say §oリスタートシーケンスを開始...\015"'

screen -p 0 -S ${SCREEN_NAME} -X eval 'stuff "say '${WAIT}'秒後にサーバ
ーを再起動します\015"'
screen -p 0 -S ${SCREEN_NAME} -X eval 'stuff "say 30秒ほど経てば再接続>可能になるので、しばらくお待ち下さい\015"'

sleep $WAIT
screen -p 0 -S ${SCREEN_NAME} -X eval 'stuff "stop\015"'

sleep 10

$STARTSCRIPT

```

以上を<kbd>Cmd</kbd>+<kbd>V</kbd>でペーストして`:wq`。

## サーバー起動

```
minecraft/
L   backup.sh
L   restart.sh
L   start.sh
L   server/
    L   paper.jar
```

こんなファイル構成になっているはずです。

[[dl|screenを使う]]
|ここからは`screen`で画面を切り替えます。
|
| |操作|キー・コマンド|
| |---|---|
| |画面一覧|`screen -ls`|
| |アタッチ|`screen -r (PID)`|
| |デタッチ|`control+A` -&gt; `control+D`
| |キル|`screen kill <PID>`|
|
### 起動してみる

```bash
bash start.sh
screen -r
```

`start.sh`はサーバーを`screen`で起動しますから、`screen -r`で **アタッチしないとサーバーは見れません。(裏では動いています)**

すると、途中で**利用規約に同意してほしい旨のメッセージが出て、サーバーが止まります。**

```
minecraft/
L   server/
    L   eula.txt
    L   paper.jar
L   backup.sh
L   restart.sh
L   start.sh
```

SFTPを見ると、こんなファイル構成になっているはずです。

:::warning シェルスクリプトはpaper.jarと別フォルダ!
サーバーが生成したファイルと、自作したファイルが混ざるのは、明らかに混乱を招きます。
シェルスクリプトはserverフォルダの外に置きましょう。
:::

### eulaの同意

```bash
cd server
vi eula.txt
```

<kbd>I</kbd>キーでINSERTモードにし、

```txt
eula=true
```

に変えてください。<kbd>Esc</kbd> -&gt; `:wq`で保存。

### 改めて起動

```bash
cd ../
bash start.sh
screen -r
```

サーバーが起動するはずです。

```
minecraft/
L   server/
    L   cache/
    L   logs/
    L   plugins/
    L   world/
    L   world_nether/
    L   world_the_end/
    L   ...
    L   eula.txt
    L   paper.jar
L   backup.sh
L   restart.sh
L   start.sh
```

こんなファイル構成になっているはずです。

### サーバー設定の変更

```bash
cd server
vi server.properties
```

人数などを変えてください。

## Termiusのスニペットに登録

Termiusのスニペット機能に以下を登録しましょう。

### 「サーバー起動」

```bash
cd /home/minecraft && bash start.sh
```

### 「サーバー再起動」

```bash
cd /home/minecraft && bash restart.sh
```

### 「アタッチ」

```bash
screen -r
```

:::info
次のページで、自動でバックアップするようにします。
:::
