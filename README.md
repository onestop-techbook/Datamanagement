# ワンストップ データ管理

## 概要説明
ワンストップ　データ管理

## この本の目的
あなたが持っているたくさんのデータ、ファイル、どうやって整理していますか？

データを保存、管理していくにあたって知っておくと幸せ（効率的、あるいは安心）
になれる様々なノウハウをまとめてみませんか？

なぜ保管、バックアップするのか、あるいはそもそも管理しなければならないのか。

どうやって保管するのか、バックアップの方法などを整理します。

RAIDやオンラインストレージを使っておけば安心なのか？

そういった内容を取り扱います。

目次メモはこちら。自由に編集、追加ください。

https://hackmd.io/KDDM2w3uT_m9y6FlOExydg

文章に起こすことで整理される側面もあるでしょう。
他の人と共有しやすくなることもあるでしょう。
それを見て、行動を起こす人がいるかもしれません。

1ページからでも構いません。執筆者の仲間入りです。
5ページ書けますか？まとまった量で読み応えありますね。
10ページ書きますか？どんとこい。
そして、あなたの本を技術書典に参加する1万人（あるいはそれ以上）に届けませんか？

## 執筆・配布スケジュール

* 募集開始・環境構築：2020月5月15日
* マッハ版本文初稿：2020年6月30日
* 章目次確定：2020年x月xx日
* 本文初稿：2020年XX月XX日
* レビュー＆追記：2020年X月X日
* オンライン発行：2020年X月X日
* 物理本発行:予定は未定

## 著者紹介兼あとがき
Contributers.re内に、テンプレートに従って記入ください。

## 執筆にあたってのお願い
CIでコンパイルが通ることを確認してください。エラーのまま放置はなるべくやめてください。

Confrictが発生した場合は、解決お願いします。

push -f等はやめましょう。（歴史を書き換えてはいけません。

相談事：
Issue立ててください。

雑談、ざっくばらんな相談については、Slackがあります。
参加方法は、親方まで。https://twitter.com/oyakata2438

## 執筆方法

本書は、easybooks を使って発行されています。easybooks では Markdown か Re:VIEW で記述します。

* [Markdownでの書き方](https://raw.githubusercontent.com/erukiti/easybooks/master/example/about-easybooks.md)
* [Re:VIEWチートシート](https://gist.github.com/erukiti/c4e3189dda179a0f0b73299fb5787838) を作ってみたので、参考にしてみてください。

また、プレーンテキストやWordとかでの提出も可能です。編集部にてコンバートします。

## CI
https://app.wercker.com/oyakata2438/Datamanagement/runs
でPDFが書きだされます。
一番上のBuildをクリックすると展開されるので、
Output Artifactをクリックして、Download artifactをクリックすると、
tarで固めたpdfがダウンロードできます。

## インストール

細かい準備(TeX入れたり)は[『技術書をかこう！』](https://github.com/TechBooster/C89-FirstStepReVIEW-v2)に準じます。

### Dockerを使う方法

Dockerを使うのが一番手軽です。とても面倒なTeXのインストールなどを全てDockerでやってくれるため、何も悩むことはありません。

```sh
$ docker run -t --rm -v $(pwd):/book vvakame/review:3.2 /bin/bash -ci "cd /book && yarn && yarn build"
```

このコマンドの実行が成功すれば、コンパイルされたPDFが、`.review/Onestop-Datamanagement.pdf` として出力されています。

Mac なら `open .review/Onestop-Datamanagement.pdf` で PDF を開くことができます。

### WindowsでReviewを使う方法

https://qiita.com/implicit_none/items/398c6e0bbedc8b160621
暗黙の型宣言さんが詳しく書いてくれてます。あるいは、技術同人誌を書こう‐アウトプットのススメ‐をご覧ください。

Windows10(Home/Pro問わず)であれば、WSL＋docker越しにRe:VIWEを扱う方法もあります。https://qiita.com/hoshimado/items/7592cee28c1bde545b78

※2019/11/04時点で、次の環境にて後述のdockerコマンドからコンパイル出来ることを確認済み。

<!-- (3.1指定は、2.x環境と共存のため) -->

* Microsoft Windows 10 Home Version 1903 
* Ubuntu 16.01
* Docker version 17.03.2-ce, build f5ec1e2
* Docker image : vvakame/review (tag:3.1)
* Docker image : vvakame/review (tag:3.2)

### Dockerを使わずにビルドする

* TeX をインストールする
* Ruby をインストールする
  * review gem をインストールする
* Node.js をインストールする

```sh
yarn && yarn build
```

### 権利

ベースには、[TechBooster/ReVIEW\-Template: TechBoosterで利用しているRe:VIEWのテンプレート（B5/A5/電子書籍）](https://github.com/TechBooster/ReVIEW-Template) を使っています。

  * 設定ファイル、テンプレートなど制作環境（techbooster-doujin.styなど）はMITライセンスです
    * 再配布などMITライセンスで定める範囲で権利者表記をおねがいします
