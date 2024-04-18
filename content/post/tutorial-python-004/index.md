---
title: Python を基礎から 4 - 四則演算
description: Google Colaboratory を使ったプログラム基礎
slug: tutorial-python-004
date: 2024-04-18 22:05:00+0900
categories:
    - 開発
    - Python基礎
tags:
    - プログラム
    - Python
    - Colaboratory
---

## 目的
簡単な計算を行います。

## 四則演算
### 振り返り
数値の扱いには前回のページで紹介した int 型を利用します。

```python
number = 30
print (number)

# 出力> 30
```

### 演算
- 足し算: `+`
- 引き算: `-`
- 掛け算: `*` (注意!)
- 割り算: `/`
- 割り算(余り): `%`

を利用します。

以下が例です。

```python
# 足し算 (320 + 430)
print (320 + 430)

# 出力> 750
```

```python
# 引き算 (320 - 430)
print (320 - 430)

# 出力> -110
```

```python
# 掛け算 (320 x 430)
print (320 * 430)

# 出力> 137600
```

```python
# 割り算 (20 ÷ 10)
print (20 / 10)

# 出力> 2.0
```

```python
# 割り算(余り) (24 ÷ 10)
print (24 % 10)

# 出力> 4
```

`+` では文字列の結合ができます。
```python
print ("30" + "円")

# 出力> 30円
```

当然変数も利用できます。
```python
# 数値の定義
number_1 = 24
number_2 = 30

print (number_1 + number_2)

# 出力> 54
```

---
Last Code Checked: 2024/4/17 by [mint73](https://github.com/mint73)
