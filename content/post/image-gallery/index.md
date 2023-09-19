---
title: イメージギャラリー
description: Markdown を利用して美しいイメージギャラリーを作成する
date: 2023-09-19 00:00:00+0000
image: 2.jpg
---

この Hugo の Stack テーマは Markdown を利用することで美しいイメージギャラリーを作成することができます。これは、 [PhotoSwipe](https://photoswipe.com/) を採用し、構文は [Typlog](https://typlog.com/) から影響を受けています。

この機能を利用するには、 Markdown ファイルと同一のディレクトリ内に画像を入れる必要があります。 Hugo のページバンドル機能を利用して、画像の寸法を読み取るためです。**外部の画像はサポートされていません。**

## 構文

```markdown
![Image 1](1.jpg) ![Image 2](2.jpg)
```

## 結果

![Image 1](1.jpg) ![Image 2](2.jpg)

> こちらは [Unsplash](https://unsplash.com/) 上でアップロードされている [mymind](https://unsplash.com/@mymind) さんと [Luke Chesser](https://unsplash.com/@lukechesser) さんの画像を利用しました。