---
title: Markdown 構文ガイド
description: Sample article showcasing basic Markdown syntax and formatting for HTML elements.
slug: markdown-syntax
date: 2023-09-20
categories: 
    - テーマ
    - 構文
    - チュートリアル
tags: 
    - markdown
    - css
    - html
    - テーマ
    - 翻訳
---

この記事では Hugo ファイルで使うことのできる一般的な Markdown 構文のサンプルを CSS で装飾された一般的な HTML 要素と一緒に紹介します。

<!--more-->

## 見出し

こちらは HTML の `<h1>`—`<h6>` 要素に相当する6種類の見出しを使用できます。 `<h1>` が最大の見出しで、 `<h6>` に近づくほど小さくなっていきます。

# H1
## H2
### H3
#### H4
##### H5
###### H6

## 段落

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin re plis aut quas inctum laceat est volestemque commosa as cus endigna tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am facea corem alique molestrunt et eos evelece arcillit ut aut eos eos nus, sin conecerem erum fuga. Ri oditatquam, ad quibus unda veliamenimin cusam et facea ipsamus es exerum sitate dolores editium rerore eost, temped molorro ratiae volorro te reribus dolorer sperchicium faceata tiustia prat.

Itatur? Quiatae cullecum rem ent aut odis in re eossequodi nonsequ idebis ne sapicia is sinveli squiatum, core et que aut hariosam ex eat.

## ブロック引用

The blockquote element represents content that is quoted from another source, optionally with a citation which must be within a `footer` or `cite` element, and optionally with in-line changes such as annotations and abbreviations.

### 出典なしのブロック引用

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **ノート** ブロック構文では、 *Markdown 構文* を利用可能です。

### 出典ありのブロック引用

> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

## テーブル

Tables aren't part of the core Markdown spec, but Hugo supports supports them out-of-the-box.

   名前 | 年齢
--------|------
    Bob | 27
  Alice | 23

### テーブル内のインライン Markdown

| 斜字   | 太字     | コード   |
| -----  | -------- | -------- |
| *斜字* | **太字** | `コード` |

| A                                                        | B                                                                                                             | C                                                                                                                                    | D                                                 | E                                                          | F                                                                    |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|------------------------------------------------------------|----------------------------------------------------------------------|
| Lorem ipsum dolor sit amet, consectetur adipiscing elit. | Phasellus ultricies, sapien non euismod aliquam, dui ligula tincidunt odio, at accumsan nulla sapien eget ex. | Proin eleifend dictum ipsum, non euismod ipsum pulvinar et. Vivamus sollicitudin, quam in pulvinar aliquam, metus elit pretium purus | Proin sit amet velit nec enim imperdiet vehicula. | Ut bibendum vestibulum quam, eu egestas turpis gravida nec | Sed scelerisque nec turpis vel viverra. Vivamus vitae pretium sapien |

## コードブロック
### Code block with backticks

```html
<!doctype html>
<html lang="ja">
<head>
  <meta charset="utf-8">
  <title>HTML5 資料例</title>
</head>
<body>
  <p>テスト</p>
</body>
</html>
```

### Code block indented with four spaces

    <!doctype html>
    <html lang="ja">
    <head>
      <meta charset="utf-8">
      <title>HTML5 資料例</title>
    </head>
    <body>
      <p>テスト</p>
    </body>
    </html>

### Diff code block

```diff
[dependencies.bevy]
git = "https://github.com/bevyengine/bevy"
rev = "11f52b8c72fc3a568e8bb4a4cd1f3eb025ac2e13"
- features = ["dynamic"]
+ features = ["jpeg", "dynamic"]
```

### 1行コードブロック

```html
<p>A paragraph</p>
```

## リスト形式

### 順序のあるリスト

1. First item
2. Second item
3. Third item

### 順序がないリスト

* List item
* Another item
* And another item

### 入れ子型リスト

* 果物
  * りんご
  * オレンジ
  * バナナ
* 乳製品
  * 牛乳
  * チーズ

## その他の要素 — abbr, sub, sup, kbd, mark

<abbr title="Graphics Interchange Format">GIF</abbr> はビットマップ画像形式です。

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

<kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Delete</kbd> を押すことでセッションを終了できます。

多くの<mark>サラマンダー</mark>は夜行性で、昆虫やミミズ、その他の生物を狩ります。