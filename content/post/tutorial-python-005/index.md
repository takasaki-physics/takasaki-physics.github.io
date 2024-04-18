---
title: Python を基礎から 5 - 入力を受け取ろう
description: Google Colaboratory を使ったプログラム基礎
slug: tutorial-python-005
date: 2024-04-18 22:05:05+0900
categories:
    - 開発
    - Python基礎
tags:
    - プログラム
    - Python
    - Colaboratory
---

## 目的
ユーザーからの入力を受け取ります。

これで、コード内で定義していない数値を扱うことができます。

## 入力
`input()` を利用します。

```python
text = input("文字列を入力してください: ")

# 出力> 文字列を入力してください: 
# ("りんご" と入力する)

print("文字: " + text)
# 出力> 文字: りんご
```

## 電卓を作ろう
前回の記事と組み合わせることで、電卓を作ることができます。

```python
number_1 = input("1つめの数を入力してください: ")
number_2 = input("2つめの数を入力してください: ")

# 入力した文字を数字に変換して計算
# (入力時に文字を入れるとエラーになります)
print(int(number_1) + int(number_2))
```

---
Last Code Checked: 2024/4/17 by [mint73](https://github.com/mint73)
