# Minecraft Kids

A fansite of Minecraft for kids.

こどものためのマインクラフトまとめサイト。（現在はティザーサイトのみ公開中）  
稼働サイトはWordPressで実装予定ですが、静的コンテンツやテーマ等の制作物は、基本的に全てこちらにアップしていきます。

![](screenshots/teaser.png?raw=true)

## URL

[http://minecraftkids.jp](http://minecraftkids.jp)

## Requrements（制作ツール）

- WordPress
- _s
- Bootstrap 3.1.1
- JQuery 1.9.0 or later
- Sketch 3.1.1 or later

## 制作過程（随時更新中）

1. [ローカル仮想環境の構築](#user-content-ローカル仮想環境の構築)
2. [ティザーサイトの作成](#user-content-ティザーサイトの作成)
	- [ティザーサイトのデザインカンプ作成](#user-content-ティザーサイトのデザインカンプ作成)
	- [ティザーサイトのコーディング](#user-content-ティザーサイトのコーディング)

### ローカル仮想環境の構築

ローカル仮想環境の構築については、同時期に進行中の[littlebird-theme](https://github.com/littlebirdjp/littlebird-theme)と全く同じ手順で行なったため、ここでは説明を割愛させていただきます。  
詳しくは、littlebird-themeの[ローカル仮想環境の構築](https://github.com/littlebirdjp/littlebird-theme#user-content-%E3%83%AD%E3%83%BC%E3%82%AB%E3%83%AB%E4%BB%AE%E6%83%B3%E7%92%B0%E5%A2%83%E3%81%AE%E6%A7%8B%E7%AF%89)をご確認ください。

### ティザーサイトの作成

WordPressでの実装前に、静的なティザーサイトとして予告ページを公開することにしました。  
ティザーサイトは、シンプルな構成のシングルページとなりますが、Sketchでデザインカンプを作成し、その後HTML + Sass/Compassでコーディングを行う流れで作成しています。

#### ティザーサイトのデザインカンプ作成

![](screenshots/screenshot01.png?raw=true)

[littlebird-site](https://github.com/littlebirdjp/littlebird-site)の時と同様、Sketchのアートボードを使って、モバイル版とデスクトップ版それぞれのデザインカンプを、1枚のページ内に作成しました。  
デザイン上はモバイル版とデスクトップ版の2つがあれば十分だったのですが、今回は制作者の検証機がiPhone 6 Plusになってしまった関係上、iPhone5, iPhone 6 Plus, Desktopの3枚のアートボードを作成しました。  
これは、Sketch Mirrorを使って実機確認する際に、検証端末ぴったりのサイズで作らないと、厳密な再現が行えないためです。

ティザーサイトでは、基本的なコンセプトとComing Soon（近日公開）ということが伝わればいいので、ロゴマークとタイトル、背景画像を使って「マインクラフト + こども」というサイトの基本テーマが伝わるデザインになるように意識しました。

本サイトのデザインでは、ヘッダー等のデザインを赤バック + ロゴ＆タイトルという色構成にする予定ですが、全面に赤を使うとドギツい印象になるため、マインクラフトのDirt（土）ブロックを模した茶色いパターン背景に変更しました。それに伴って、メインタイトルにも読みやすく白ボーダーを付けるなどの微調整を加えてあります。

#### ティザーサイトのコーディング

本公開時にはBootstrapで実装する予定ですが、今回はシンプルなティザーサイトなので、フレームワークは使わず、フルスクラッチでざっくりとコーディングしました。  

ロゴ、タイトル、背景などの画像パーツは、iPhone 6 Plusなどdevice pixel ratio:3の端末にも対応できるよう、Sketchで3倍サイズに書き出し、ブレークポイントごとにサイズ指定しています。

ブレークポイントは、Bootstrapと同じ段階設定で変数化していますが、このページでは480px切り替えのみ使用しています。CSSの設計は一応BEM風にしてありますが、ページ内の要素数が少ないのであまり意味はないかもしれません。

ソーシャルボタン回りでは、Media Queriesを用いて、デスクトップ版の時だけGoogle+ボタンを表示、モバイル版の時だけLINEボタンを表示するように、表示項目を切り替えています。


