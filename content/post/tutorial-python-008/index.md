---
title: Python を基礎から 8 - 配列
description: Google Colaboratory を使ったプログラム基礎
slug: tutorial-python-008
date: 2024-07-12 17:24:00+0900
categories:
    - 開発
    - Python基礎
tags:
    - プログラム
    - Python
    - Colaboratory
---

## 目的
1次元配列を処理できるようにします。

(配列は array のことを示す場合もありますが、ここでは list の話をします)

## 1次元配列
そもそも、1次元配列とは Excel の横列または縦列だけを利用するようなイメージです。

ここでは例として、以下のように本を積み重ねる場合を考えてみましょう。

例:
| 本のタイトル |
| - |
| Murder on the Orient Express |
| The ABC Murders |
| And Then There Were None |
| Dead Man's Folly |

配列をコードで表す場合は、`array1 = ["a", "b", "c", "d"]` のように宣言することができます。

また、`array1[0]` や `array1[1]` のように指定することで、それぞれの要素 `"a"` や `"b"` などを取り出すことができます。

これを先程の例で示すと、以下のコードになります。

例:
```python
books = ["Murder on the Orient Express", "The ABC Murders", "And Then There Were None", "Dead Man's Folly"]

print(books) # 配列全体を出力
# 出力> ['Murder on the Orient Express', 'The ABC Murders', 'And Then There Were None', "Dead Man's Folly"]

print(books[0]) # 配列の1番目を出力 (配列は0から数えるので、1番目を出力する場合は0を指定する)
# 出力> Murder on the Orient Express

print(books[1]) # 配列の2番目を出力 (配列は0から数えるので、2番目を出力する場合は1を指定する)
# 出力> The ABC Murders

# 配列を利用してそれぞれの要素を出力
for i in range(len(books)): # len(books) は配列の長さ。これは1から数えるので、4が返される
  print(books[i])
# 出力>
# Murder on the Orient Express
# The ABC Murders
# And Then There Were None
# Dead Man's Folly
```

数値を扱うことも可能です。

例:
```python
numbers = [6, 1, 52, 30, 3]

print(numbers[0])
# 出力> 6

# 配列の数値を利用して計算もできます。
cal = numbers[0] + numbers[1]
print(cal)
# 出力> 7

# 小さい順に並び替える
print(numbers) # 並び替え前
# 出力> [6, 1, 52, 30, 3]
numbers.sort() # 並び替え
print(numbers)
# 出力> [1, 3, 6, 30, 52]
```

これで一通りのガイドは終わりとなります。

応用的な内容や、2次元配列などについては追記するかもしれません。

---
Last Code Checked 2024/7/12 by [mint73](https://github.com/mint73)
