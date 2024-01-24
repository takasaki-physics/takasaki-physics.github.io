---
title: Linux環境設定
description: 私的Linux設定方法
slug: linux-setting
date: 2023-10-11
categories: 
    - 開発
tags: 
    - Linux
    - ソフトウェア
    - 開発環境整備
---

こんにちは。<br />
今回は私的Linux環境の準備方法を説明します。<br />

## ソフト開発関係
### VSCode
テキストエディタです。<br />

VimとかKateとかもありますけど、私はVSCodeが最推しですね。<br />
比較的軽量で、拡張機能によって豊富な機能を搭載でき、なおかつシンプルなため、初心者から神まで御用達のツールとなっています。<br />
本職のプログラマーやWebデザイナーなどにも人気です。<br />
(皆さんは個人開発だと思うのであまり関係ありませんが、商用利用の際もライセンスが軽いので使いやすいです。)<br />

さて、VSCodeはLinux(Debian系)だと様々な方法でインストールできますが、いちばん簡単な方法だと、```apt```を使った方法になります。<br />

参考: [Qiita - UbuntuにVSCodeをインストールする3つの方法](https://qiita.com/yoshiyasu1111/items/e21a77ed68b52cb5f7c8)<br />

#### インストール
```shell
# curlのインストール
sudo apt install curl

# curlでMicrosoftのキーをダウンロード
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg

# レポジトリを登録する
sudo install -o root -g root -m 644 microsoft.gpg /etc/apt/trusted.gpg.d/
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'

# インストール
sudo apt install apt-transport-https
sudo apt update
apt list code
apt list -a code
sudo apt install code
```

#### 起動
```shell
code
```

### Opera
ブラウザです。<br />

参考: [UbuntuにOperaをインストールする方法](https://tutorialcrawler.com/ubuntu-debian/ubuntu-20-04%E3%81%ABopera%E3%83%96%E3%83%A9%E3%82%A6%E3%82%B6%E3%82%92%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E3%81%99%E3%82%8B%E6%96%B9%E6%B3%95/)<br />

#### インストール
```shell
# キーのダウンロード
wget -qO- https://deb.opera.com/archive.key | sudo apt-key add - 
echo deb https://deb.opera.com/opera-stable/ stable non-free | sudo tee /etc/apt/sources.list.d/opera.list 

# インストール
sudo apt update
sudo apt install opera-stable
```

#### 起動
```shell
opera --lang=ja
```

#### 言語設定(推奨)
ちなみに、初期状態でデスクトップアイコンから起動しても英語なので、.desktopファイルを少しいじる必要があります。<br />

参考: [Opera Forums - UIの言語を変える方法](https://forums.opera.com/topic/58114/can-t-change-ui-language-no-option-display-opera-in-that-language/4)(英文)<br />

```shell
cat /usr/share/applications/opera.desktop
# [Desktop Entry]
# Version=1.0
# Name=Opera
# GenericName=Web browser
# Comment=Fast and secure web browser
# TryExec=opera
# Exec=opera %U
# Terminal=false
# Icon=opera
# ...

# この"Exec=opera %U"の部分を"Exec=opera --lang=ja %U"にvimなどで変える
sudo vim /usr/share/applications/opera.desktop
```

## グラフィック系
### Krita
イラスト系最高傑作ソフトです。<br />
開発者の皆様はあまり使わないかも知れませんが、私はイラストを描くことが好きなので、紹介させていただきます。<br />

```apt```版はバージョンがかなり古いので、公式からインストールしましょう。<br />

参考: [Krita Docs - Kritaのインストール方法](https://docs.krita.org/ja/user_manual/getting_started/installation.html#linux)

#### インストール
1. [Krita公式サイトのダウンロードページ](https://krita.org/jp/download-jp/krita-desktop-jp/)からappimageをダウンロードします。
1. krita.appimageが入っているディレクトリ内で以下のコマンドを打ちます。
```shell
chmod a+x ./krita.appimage
```

#### 起動
```shell
./krita.appimage
```

エラーが起こる場合はそれをインストールしましょう。<br />
.desktopファイルを作っておくとGUIからも起動できるので楽です。<br />

## コンソール系
### .NET SDK
C#やVB.NET、F#を動作させるのに必要なSDKです。<br />
今回はDebian12のインストール方法を記載します。<br />
それ以外のOSの場合は下のURLを参考にしてください。<br />

参考: [Microsoft - .NETをインストールする](https://learn.microsoft.com/ja-jp/dotnet/core/install/)<br />

#### インストール
```shell
# キーのインストール
wget https://packages.microsoft.com/config/debian/12/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
rm packages-microsoft-prod.deb

# SDKのインストール
sudo apt-get update && \
  sudo apt-get install -y dotnet-sdk-7.0

# ランタイムのインストール
sudo apt-get update && \
  sudo apt-get install -y aspnetcore-runtime-7.0
```

#### 新しいコンソールプロジェクトの作成
```shell
dotnet new console -o プロジェクト名
```

#### 新しいBlazor wasmプロジェクトの作成
```shell
dotnet new blazorwasm -o プロジェクト名 --pwa
```

#### プロジェクトの起動
```shell
dotnet watch run
```

### neofetch
端末情報が見れるソフトです。<br />
メモリ使用量とかも見れるので便利です。<br />

#### インストール
```shell
sudo apt install neofetch -y
```

#### 起動
```shell
neofetch
```

### tint
テトリスです。<br />

#### インストール
```shell
sudo apt install tint -y
```

#### 起動
```shell
tint
```

### sl
電車が走るコマンドです。<br />
中断できないので```ls```コマンドと間違えたときに邪魔なコマンドです。<br />

#### インストール
```shell
sudo apt install sl
```

#### 起動
```shell
sl
```

```sl -l```にすると長くなります。<br />
<kbd>Ctrl</kbd> + <kbd>C</kbd> でも中断できないという謎仕様です。<br />

### cmatrix
コマンドライン上でマトリックスできるコマンドです。<br />
人気コマンド。<br />

#### インストール
```shell
sudo apt install cmatrix
```

#### 起動
```shell
cmatrix
```

```cmatrix -C red```のように色を変えることもできます。<br />
