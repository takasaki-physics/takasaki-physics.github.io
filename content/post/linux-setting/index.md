---
title: Linux環境設定
description: 私的Linux設定方法
slug: linux-setting
date: 2023-10-05
categories: 
    - 開発環境
tags: 
    - Linux
    - ソフトウェア
---

こんにちは。<br />
今回は私的Linux環境の準備方法を説明します。<br />

## ソフト開発関係
### VSCode
テキストエディタです。<br />
Kateとか(昔の)Atomとかもありますけど、私はVSCodeが最推しですね。<br />

比較的軽量で、拡張機能によって豊富な機能を搭載でき、なおかつシンプル(ごちゃごちゃしていない)ため、初心者から神まで御用達のツールとなっています。<br />
当然、本職のプログラマーやWebデザイナーなどにも人気です。<br />
(皆さんは個人開発だと思うのであまり関係ありませんが、商用利用の際もライセンスが軽いので使いやすいです。)<br />

さて、VSCodeはLinuxだと様々な方法でインストールできますが、いちばん簡単な方法だと、```apt```を使った方法になります。<br />
(当然FlatpakやSnapを使った方法もあります。)<br />

#### インストール
```shell

```

#### 起動
```shell
code
```

### Opera
ブラウザです。<br />
私は初めてパソコンを触ったときからずっと愛用しています。
誕生は20年以上前と深い歴史のあるブラウザです。<br />
(現代の主要(top5)ブラウザでは最古参<br />
Opera: 1996年<br />
Firefox: 1998年(beta版)<br />
Safari: 2003年<br />
Chrome: 2008年<br />
Edge: 2015年)<br />

ChromeベースでHTMLレンダリングエンジンはBlinkを採用しているため、Chromeと同様の機能が使えつつ、更にサイドバーのSNSやAIの機能などの便利機能を搭載しているためとても使いやすいです。当然広告ブロック機能も搭載していますよ。(ChromeとEdgeへの煽り)<br />
近年では世界初のゲーミングブラウザのOpera GXも出しています。(GXはLinuxでは使えません。)<br />

公式にインストール方法が書かれているので、それで準備をしましょう。<br />

ちなみに、この状態で起動しても英語なので、.desktopファイルを少しいじる必要があります。<br />


## グラフィック関連
### Krita
イラスト系最高傑作ソフトです。<br />
開発者の皆様はあまり使わないかも知れませんが、私はイラストを描くことが好きなので、紹介させていただきます。<br />

```apt```版はバージョンがかなり古いので、公式からインストールしましょう。<br />

#### インストール
- Krita公式サイトのダウンロードページからappimageをダウンロードする。
- krita.appimageが入っているディレクトリ内で以下のコマンドを打つ。
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

公式にインストール方法が書かれているため、そちらを参考にしてください。

#### 新しいコンソールを追加
```shell
dotnet new console -o プロジェクト名
```

#### 新しいBlazor wasmを追加
```shell
dotnet new blazorwasm -o プロジェクト名 --pwa
```

#### プロジェクトを作動
```shell
dotnet watch run
```

### neofetch
端末情報が見れるソフトです。<br />
メモリ使用量とかも見れるので微妙に便利です。<br />

#### インストール
```shell
sudo apt install neofetch -y
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

#### 起動
```shell
neofetch
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
