---
title: 数式の書き方
description: KaTeXを使った数式の書き方について
date: 2023-09-19 00:00:00+0000
math: true
---

こちら Stack は [KaTeX](https://katex.org/) を利用した数式の記述をサポートしています。

**ですが、この機能は標準で使用できるわけではありません。** しかし posts の冒頭部の記述に `math: true` を追加するだけで利用可能になります。または、プロジェクト内の `config.toml` に `math = true` を追加することで常に利用可能になります。

## インライン数式

こちらはインライン数式の例です: $\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…$

```markdown
$\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…$
```

## ブロック数式

$$
    \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$

```markdown
$$
    \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$
```

$$
    f(x) = \int_{-\infty}^\infty\hat f(\xi)\,e^{2 \pi i \xi x}\,d\xi
$$

```markdown
$$
    f(x) = \int_{-\infty}^\infty\hat f(\xi)\,e^{2 \pi i \xi x}\,d\xi
$$
```
