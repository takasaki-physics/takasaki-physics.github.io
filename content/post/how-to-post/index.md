---
title: 投稿しよう!
description: このサイトに記事を投稿する
slug: how-to-post
date: 2023-09-22 00:00:00+0000
categories:
    - チュートリアル
---

# 記事の投稿方法について

## 前提条件
- GitHub アカウントを保持している
- Git の使い方がなんとなくわかる
- Markdown の書き方がわかる

## TL; DR
1. [本サイトのレポジトリ](https://github.com/takasaki-physics/takasaki-physics.github.io)をフォーク
1. *content/post/* ディレクトリ内に適当な名前のファイルを配置し、その中に *index.md* を作成する。
1. 記事の内容を Markdown 形式で記述する。(このとき、ページタイトルなどの情報を追加する。)

## ブラウザ上で作業する方法
こちらの方法では、 GitHub を使い、ブラウザ上で動く Visual Studio Code (以下 VSCode) を使用して作業を進める方法を記述します。<br />
すべてブラウザ上で完結するため初期設定は簡単です。<br />
しかし、 VSCode の起動にやや時間がかかってしまうのと、インターネットが使えない環境で作業ができないというデメリットもあります。<br />

### レポジトリをフォークする
1. GitHub アカウントにログインします。
1. [GitHub-高崎高校物理部](https://github.com/takasaki-physics/takasaki-physics.github.io)にアクセスします。
1. レポジトリをフォークします。
<details>
<summary>参考画像</summary>

![Image 1](1.png)
![Image 2](2.png)
</details>

### VSCodeの起動
GitHub を使ってブラウザ上で VSCode を起動する方法は2種類あり、 Codespaces を使う方法と github.dev を使う方法です。<br />
Codespaces のほうがおすすめです。<br />
どちらかの方法で起動してください。<br />
起動方法は以下のとおりです。<br />

#### Codespaces の起動
起動方法は下の画像を参考にしてください。<br />
![Codespaces 起動](4.png)
高機能ですが起動に時間がかかります…<br />

#### github.dev の起動
こちらはレポジトリを開いた状態(下の画像の状態)でキーボードの <kbd>.</kbd> を押すことで起動できます。<br />
![レポジトリを開いた画面](3.png)
何故かファイルを開けないことが多いので、あまりおすすめしません。<br />

### 投稿記事を作成
ついに、投稿記事が作成できるようになりました!<br />
記事は *content/post/* ディレクトリ内に作成します。<br />
1. *content/post/* ディレクトリを開く
1. 新しいディレクトリを作成する
<br />(ディレクトリ名は英語がよいです)
1. 新規作成したディレクトリに移動する
1. *index.md* を作成する

この *index.md* 内に記事を書いていくこととなります。<br />
ただし、ページ上部に以下の記入をする必要があります。<br />
(日本語の部分は各自書き換えてください。)<br />
```
---
title: タイトルを記入
description: 説明を記入
slug: タイトルを英語で記入(英語、記号は"-"以外基本的に禁止)(これはURLにつかわれます。)
img: 同ディレクトリ内に存在する画層ファイル名を記入(なくてもいい)
date: 日付を記入(例: 2023-09-21 00:00:00+0000)
categories:
    - カテゴリーを記入(なくてもいい)
tags:
    - タグを記入(なくてもいい)
---
```
他の記事の記述方法を真似すると良いです。<br />
(*[content/post/markdown-syntax/index.md](https://github.com/mint73/takasaki-physics.github.io/blob/main/content/post/markdown-syntax/index.md?plain=1)* など)<br />

この記述のあとに通常の Markdown 形式で記述を進めてください。<br />

例:
```markdown
# タイトル
内容を記入
```
Markdown 記法や画像の使い方などに関しては他の記事でまとめられているので、そちらを参照してください。<br />

現時点で作成されたこちらのサイト内の資料
- [Markdown 構文](https://takasaki-physics.github.io/p/markdown-syntax)
- [イメージギャラリー](https://takasaki-physics.github.io/p/image-gallery)
- [数式記述](https://takasaki-physics.github.io/p/math-typesetting)
- [ショートコード](https://takasaki-physics.github.io/p/shortcodes)

Hugo Stack 本家資料
- [本家資料](https://stack.jimmycai.com/) (英文)

## コミット、プル、マージリクエスト
資料作成が終了したらコミット/プルし、その後マージリクエストを作成して反映を待ってください。<br />

マージリクエスト受諾後には自動的に GitHub Actions が動作して、サイトに新しいページが追加されます。<br />
反映まで多少時間がかかる可能性があるので、数分お待ち下さい。<br />
(数分立っても反映されない場合は、ブラウザのキャッシュが邪魔している可能性があります。<br />
その際は、 <kbd>Ctrl</kbd> + <kbd>F5</kbd> (スーパーリロード)を行ってください。)<br />

## ローカル環境で作業する方法
こちらの方法では、ローカルの VSCode と Git を使用して作業を行う方法を記述します。<br />
初期設定はブラウザ上でも行いますが、初期設定後はブラウザを使用せずに作業が簡単にできるのでおすすめです。<br />

記述中です。更新をお待ち下さい。<br />

## おまけ
余談ですが、 Codespaces を使う場合やローカルで Hugo をインストールしている場合では、 ```hugo server``` コマンドによってデプロイする前にどのような見た目になるかを見ることができます。<br />

## 終了
お疲れ様でした。<br />
初期設定は面倒ですが、2回目以降はフォークなどの作業が不要なので、比較的更新は楽になると思います。<br />

ブラウザ環境のコミット、プル、マージの方法と、ローカル環境に関してや、 ```hugo server``` コマンドに関しては
後日詳しい内容や方法を追記するかも知れません。<br />