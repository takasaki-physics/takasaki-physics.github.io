---
title: Python を基礎から 7 - 繰り返し - for 文
description: Google Colaboratory を使ったプログラム基礎
slug: tutorial-python-007
date: 2024-07-12 16:50:00+0900
categories:
    - 開発
    - Python基礎
tags:
    - プログラム
    - Python
    - Colaboratory
---

## 目的
繰り返しの処理をします。

## 繰り返し
`for i in range(N)` (`N` は数値) を利用します。

例:
```python
for i in range(4):
  print(i + " ")

# 出力> 0 1 2 3
```

`range(N)` とすると、`N-1` (`0` から数えるので、 `N` ではなく `N-1`) まで増えます。

### 繰り返し文字を出力
`Hello World!` を4回表示してみましょう。

例:
```python
for i in range(4):
  printf("Hello World!")

# 出力>
# Hello World!
# Hello World!
# Hello World!
# Hello World!
```
