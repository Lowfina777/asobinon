---
title: ステップ3. paperのインストール
---

## SFTPで接続しよう

Termiusの「SFTP」を開いてください。

## paperのダウンロード



## 起動スクリプトを作る

```bash
vi start.sh
```

Vimを使うことになります。

[[big]]
|Vimを使うことになります。

[[dl|Vimの使い方]]
|<kbd>I</kbd>キーで編集(INSERT)モードになり、<kbd>Esc</kbd>で編集終わり、`:wq`で保存します。

### `start.sh`

```bash
#!/bin/bash

cd $HOME/server

screen -md -S minecraft java -XX:+UseBiasedLocking -XX:+DisableExplicitGC -XX:+UseTLAB -Xms2G -Xmx4G -XX:TargetSurvivorRatio=90 -XX:SurvivorRatio=8 -XX:MaxTenuringThreshold=4 -XX:-UseParallelGC -XX:ParallelGCThreads=2 -XX:ConcGCThreads=2 -jar paper.jar nogui

```

## 再起動スクリプトを作る

```bash
vi restart.sh
```

### `restart.sh`

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

## eulaの同意

```bash
vi eula.txt
```

`eula=true`に変えてください。

:::info
次のページで、自動でバックアップするようにします。
:::
