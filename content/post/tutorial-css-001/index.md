---
title: CSS 基礎 1 - 環境構築/準備
description: アプリケーションに彩りを
slug: tutorial-css-001
date: 2024-07-18 12:07:00+0900
categories:
    - 開発
    - CSS基礎
tags:
    - プログラム
    - ウェブアプリ
    - Css
    - 開発環境整備
---

## 目的
CSS の利用方法を解説します。

## 環境構築
### CSS とは
そもそも、CSS (Cascading Style Sheets) は HTML の装飾に利用されます。

詳細は Mozilla が作成する [CSS の基本](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/CSS_basics)を御覧ください。

### 準備
HTML ファイルは `index.html` とします。

`index.html` 内の `<head>` 要素内に `<link href="style.css" rel="stylesheet">` を追加してください。 (もしかしたら最初からあるかも)

```index.html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <!-- 略 -->
    <link href="style.css" rel="stylesheet">
  </head>
  <body>
    <!-- 略 -->
  </body>
</html>
```

続いて、CSS ファイルを `style.css` として作成します。
場所は `index.html` と同じにするのが楽です。

```directory
./
├index.html
└style.css
```

これですぐに CSS が利用できます。

### 動作確認
では、CSS がしっかりと動作するか見てみましょう。

まずは、この HTML 要素の色を変えてみましょう。

```.html
<p>りんご</p>
```

`style.css` を以下のようにしてください。

```style.css
p {
  color: red;
}
```

これで、文字の色が赤色に変化することがわかると思います。
この時点で色が変更していない場合は、環境構築がうまくいっていない可能性があるので、やり直してみてください。

### 指定方法
#### 基本指定
先ほど、サラッと紹介しましたが、CSS は以下の方法で指定します。

```.css
要素 {
  変更: 内容;
}
```

要素は、`p` や `body`、全体を指定する `:root` などがあります。

#### ID, Class 指定
また、`<p id="apple" class="fruits">りんご</p>`
このような ID は `#apple`。Class は `.fruits` のように指定できます。

また、`<p style="color: blue">青色<p>` のように直接指定することも可能です。

複数指定する場合は `,` で区切ります。

```.css
p,
#apple,
.fruits {
  background-color: blue;
}
```

#### 子要素指定
連続して指定すると、子要素だけに CSS を適応できます。

```.css
p a {
  color: yellow;
}
```

```.html
<!-- <a> 要素が <p> 要素の中にあるときだけ黄色になる -->
<p><a>黄色</a></p>

<!-- <a> 要素が <p> 要素の中にないときは黄色にならない -->
<p>黄色じゃない</p>
<a>黄色じゃない</a>
<h1><a>黄色じゃない</a></h1>
```
