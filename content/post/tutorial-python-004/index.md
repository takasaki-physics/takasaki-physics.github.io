---
title: Python を基礎から 4 - 電卓を作ろう (四則演算)
description: Google Colaboratory を使ったプログラム基礎
slug: tutorial-python-004
date: 2024-04-16 16:23:00+0900
categories:
    - 開発
    - Python基礎
tags:
    - プログラム
    - Python
    - Colaboratory
---

## 目的
電卓の作成を通して、四則演算や int への理解を深める。

## 四則演算
### 振り返り
数値の扱いには前回のページで紹介した通り、 int 型を利用します。

```python
int number = 30
print (number)

# 出力> 30
```

### 演算
- 足し算: `+`
- 引き算: `-`
- 掛け算: `*` (注意!)
- 割り算: `/`<br />
(小数点は切り下げ)
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

# 出力> 2
```

割り算は割り切れない場合は切り下げます。
```python
# 割り算 (24 ÷ 10)
print (24 / 10)

# 出力> 2
```

当然変数も利用できます。
```python
# 数値の定義
number_1 = 24
number_2 = 30

print (number_1 + number_2)

# 出力> 54
```
