---
title: GitHub CLI で GitHub と SSH 接続する
description: SSH 接続しよう
slug: 20241122-github
date: 2024-11-22 21:23:00+0900
categories:
    - 環境構築
tags:
    - プログラム
    - GitHub
---

お久しぶりです。[mint73](https://github.com/mint73) ですわ。

なぜか HTTPS 通信ができなくなったので、SSH 接続に切り替えたお話ですわ。

## インストール

### Windows

```sh
winget install --id GitHub.cli
```

このコマンドを打ったら、一度ターミナルを再起動してください。タブを消しただけではだめです、ウィンドウごと再起動してくださいね。

詳細: https://github.com/cli/cli?tab=readme-ov-file#windows

### macOS

```sh
brew install gh
```

詳細: https://github.com/cli/cli?tab=readme-ov-file#macos

### Linux

ディストリビューションごとに結構違うので、[ドキュメント](https://github.com/cli/cli/blob/trunk/docs/install_linux.md)を参考にしてください。

## アカウント連携

```sh
gh auth login --web
```

1. Git を操作するプロトコルを HTTPS にするか SSH にするか選べます。(今回は `SSH`)
1. SSH 暗号を作るかどうか聞かれます。(初めて SSH する際は作ってください)
1. ブラウザが立ち上がるので、コマンドにあるワンタイムコードを入力してください。(例: `3D41-8747` のような数字)

終わりです! :tada:

## おまけ: エディター設定

### VSCode

```sh
gh config set editor "code --wait"
```

### Vim

```sh
gh config set editor "vim"
```

## おまけ: HTTPS を SSH に切り替える方法

```sh
git remote set-url origin git@github.com:example/example.git
# 例: git remote set-url origin git@github.com:takasaki-physics/takasaki-physics.github.io.git
```

## さいごに

SSH 接続が非常に簡単にできますね。

(スクリーンショットを撮るべきでした…)

---

### 参考文献

- https://qiita.com/s_yasunaga/items/110d21828bd4f578850d
- https://qiita.com/shirokuma89dev/items/da116405f40d50c9fc99
- https://github.com/cli/cli
- https://qiita.com/ryomoucmei/items/ec8c225603ef983fc318
