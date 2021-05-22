---
title: 基本的なMarkdownの書き方
---

## 見出し

画面の右にある「目次」は、全て見出しを解析して生成されています。

[[dl|階層を守って!]]
|**見出しを「文字の大きさを変えるため」に使わないでください。**
|構造の壊れた見出しは、アクセシビリティの観点からも非常に不親切です。
|文章の主従・包含関係が把握できなくなり、保守性も悪くなります。
|数学の「集合と論理」を思い出してください。あの分野を疎かにして後悔したことがあるでしょう?

```md
# 記事タイトル(レベル1)

## その下(レベル2)

### さらにその下の階層(レベル3)

#### その下の下(レベル4)
```

## 太字

部分的に**太字**にできます。

```md
部分的に**太字**にできます。
```

## 斜体

部分的に_斜体_にできます。

```md
部分的に_斜体_にできます。
```

## リンク

[文章](https://example.com)

```md

[文章](https://example.com)

```

## コード

2つの書き方があります。

### インラインコード

`import tensorflow as tf`

```md
`import tensorflow as tf`
```

### コードブロック

複数行を書く場合は「\`\`\`言語名」と「\`\`\`」で囲みます。Docusaurusのおかげで「コピー」ボタンが付きます。

```python
entities = ["creeper", "skeleton", "zombie"]
for x in entities:
  print(x)
```

`````md
```python
entities = ["creeper", "skeleton", "zombie"]
for x in entities:
  print(x)
```
`````

Markdownを解説したい時は`md`と付けます。

#### コードブロックを入れ子にする

もし \`\`\` をコード内に書きたい時は、外側の\`を増やします。

```````md
`````
```python
# ここにコード
```
`````
```````

## 役立ちそうなリンク

* [Markdown記法/書き方 (notepm)](https://notepm.jp/help/how-to-markdown "Markdown記法/書き方（見出し・表・リンク・画像・文字色など）")
* [Markdown記法 チートシート (Qiita)](https://qiita.com/Qiita/items/c686397e4a0f4f11683d "Markdown記法 チートシート")
* [Markdownで画像を表示する (tatzyr)](https://gist.github.com/Tatzyr/3847141 "Markdownで画像を表示する")