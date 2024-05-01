---
title: Python を基礎から 6 - 条件分岐 - if 文
description: Google Colaboratory を使ったプログラム基礎
slug: tutorial-python-006
date: 2024-05-01 10:00:00+0900
categories:
    - 開発
    - Python基礎
tags:
    - プログラム
    - Python
    - Colaboratory
---

## 目的
条件分岐をします。

これにより、数値の大きさによって出力を変えることができます。

## 条件分岐
`if` を利用します。

### 比較
比較の際に利用する主なコード (比較演算子) は以下の通りです。

- `x == y` - x と y が等しい
- `x != y` - x と y が等しくない
- `x > y` - x が y より大きい
- `x < y` - x が y 未満
- `x >= y` - x が y 以上
- `x <= y` - x が y 以下

例:
```python
number = 100
if number == 100:
    printf("number is 100.") # number が100だったときに処理
```
`number` の数値が`100`のときは文字が出力され、`100`以外のときは出力がされません。

### 複雑な比較
`if` でなかった場合は、 `else` や `elif` を利用します。

例:
```python
number = 100
if number == 100:
    printf("number is 100.") # number が100だったときに処理
else:
    printf("number is not 100.") # number が100以外のときに処理
```

```python
number = 100
if number == 100:
    printf("number is 100.") # number が100だったときに処理
elif number == 120:
    printf("number is 120.") # number が120だったときに処理
```

本資料では解説しませんが、更に複雑な条件分岐に関しては、 `match` 文を利用します。
これは、他の言語に当たる `switch-case` 文のようなものです。
