---
title: ステップ4. 自動でバックアップさせる
---

## バックアップフォルダ

バックアップは`/home/minecraft/world_backup`に入れます。

## バックアップを自動化

```bash
vi backup.sh
```

### `backup.sh`

```bash
#!/bin/bash

WAIT=15
STARTSCRIPT=$HOME/start.sh
SCREEN_NAME='minecraft'

screen -p 0 -S ${SCREEN_NAME} -X eval 'stuff "say '${WAIT}'秒後にサーバ
ーを再起動します\015"'
screen -p 0 -S ${SCREEN_NAME} -X eval 'stuff "say 1分ほど経てば再接続可
能になるので、しばらくお待ち下さい\015"'

sleep $WAIT
screen -p 0 -S ${SCREEN_NAME} -X eval 'stuff "stop\015"'

sleep 20

cd /home/minecraft/world_backup
DIR=`date '+%Y%m%d_%H%M'`
tar -zcvf $DIR.tar.gz -C $HOME/server world

$STARTSCRIPT

```

## cronに登録

## 参考

- <https://qiita.com/uuu_n/items/17bcb08cbdf2aa90dc11>

:::info
次のページで、プラグインをインストールします。
:::
