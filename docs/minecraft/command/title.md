# title

| 項目 | 内容 |
| --- | --- |
| コマンド | `title` |
| 目的 | 画面上のタイトル文字を管理する |
| 必要な権限レベル | 1 |
| コマブロで実行 | 可能 |
| 適用対象 | プレイヤー |

## 構文

[[dl|指定したプレイヤーのタイトルを消去する]]
|```
|/title <ターゲット> clear

[[dl|指定したプレイヤーのタイトルの設定をリセットする]]
|```
|/title <ターゲット> reset**
|```

[[dl|指定したプレイヤーのタイトルとサブタイトルの表示時間を設定する]]
|```
|/title <ターゲット times <フェードイン時間> <表示時間> <フェードアウト時間>
|```

[[dl|指定したプレイヤーのサブタイトルの内容を変更・設定する]]
|```
|/title <ターゲット> subtitle <テキスト>
|```

[[dl|指定したプレイヤーのメインタイトルの内容を設定し表示する]]
|```
|/title <ターゲット> title <テキスト>
|```

[[dl|指定したプレイヤーのアクションバーにテキストを表示する]]
|```
|/title <ターゲット> actionbar <テキスト>

## 引数

[[dl|<プレイヤー>]]
|タイトルを表示するプレイヤーを指定する。プレイヤー名もしくはターゲットセレクターでないといけない。

[[dl|<テキスト>]]
|画面上に表示するタイトルの内容を書く。**Java版のようなJSON文書は使えないので、装飾するには看板のように§(セクション)記号を使う必要がある。**
|(つまり、Java版用のタイトル生成ツールを使っても、BEにはJSONがそのまま表示されてしまうということ)

[[dl|<フェードイン時間>、<表示時間>、<フェードアウト時間>]]
|タイトルがフェードインする時間、不透明な状態で表示される時間、フェードアウトする時間を**ゲーム内tick数で指定**する。20で1秒である。
|`-2147483648`から`2147483647`の間の数値しか指定できないが、0未満の数は0として扱われる。
|指定しない(またはリセットされた)場合は、10(0.5秒)、70(3.5秒)、20(1秒)になる。  
| 
|なお、actionbarモードで表示する**アクションバーのタイトルの表示時間は変更できない。**

## 実行結果

引数が正しく指定されていない場合、プレイヤーが見つからない場合は失敗する。

成功すると:

-   clear : 指定したプレイヤーの画面のタイトルを消去する。そのプレイヤーに現在タイトルが表示されていない場合は効果がない
-   reset : 指定したプレイヤーに**設定されているサブタイトルと表示時間**をリセットする
-   times : 指定したプレイヤーの、現在表示されている、もしくはこれから表示するタイトルのフェードイン・表示・フェードアウト時間を設定する
-   title : 指定したプレイヤーにタイトルを表示する、もしくは現在表示されているメインのタイトルを変更する。表示したら、設定されているサブタイトルは空白にされる(表示時間等はリセットしない)。つまり連続してtitleモードを実行するとサブタイトルは消える
-   actionbar : 指定したプレイヤーのアクションバー(手持ちバーの上のテキスト)にテキストを表示する、もしくは現在のアクションバーの内容を変更する

## 使用例

1.  `/title @a times 22 90 28` : 全てのプレイヤーのタイトルのフェードイン・表示・フェードアウト時間を1.1秒・4.5秒・1.4秒に設定する
2.  `/title @a subtitle ABC` : 全てのプレイヤーに「ABC」というサブタイトルを設定する
3.  `/title @a title DEF` : 全てのプレイヤーに「DEF」というタイトルを設定して表示する。**と同時にサブタイトルも表示される**
4.  これでサブタイトルがリセットされてしまうので、もう一度同じタイトルを表示したい場合は、もう一度`/title @a subtitle ABC`を実行する必要がある
