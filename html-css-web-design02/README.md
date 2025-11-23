### ほんの一手間で劇的に変わる HTML & CSS と Web デザイン実践講座 Mana

#### [c105 column 英単語の省略形](https://www.notion.so/d6da96eee5fb4ad199508789eae13ac6?source=copy_link#2ba64bd77a0780a290a3ca1295f722aa)

#### [c105 よく使われるクラス名一覧](https://www.notion.so/d6da96eee5fb4ad199508789eae13ac6?source=copy_link#2ba64bd77a078018ab75d2215ded69f9)

#### [c106 column 英単語を繋げる時の書き方](https://www.notion.so/d6da96eee5fb4ad199508789eae13ac6?source=copy_link#95e04afd458d4a4e9dd5afd1b32d3185)

#### [c107 ベンダープレフィックスとは](https://www.notion.so/Personal-Home-fa46a188398f47559d85717b879cae44?source=copy_link#2ba64bd77a0780fa96ddfb18bf2e4454)

c1-8 デベロッパーツールを使いこなす

### c2 LP で学ぶレスポンシブデザインとフォント

#### c203

- 背景画像は 1200 ~ 3000px くらいが品質維持して表示できる。
- 画像ファイル圧縮サイト
  - [Shrink Me](https://shrinkme.app/)
  - [Compressor.io](https://compressor.io/)

#### c204

- [Web フォント](https://www.notion.so/Personal-Home-fa46a188398f47559d85717b879cae44?source=copy_link#0f285b88359541708be62d62e23f14d4)
- フォントの組み合わせ例

#### [c205 アイコンフォントの使い方](https://www.notion.so/Personal-Home-fa46a188398f47559d85717b879cae44?source=copy_link#0b8818e6cab4457cb33f75ccfdad0fc4)

#### c206 スマートフォンでの閲覧に対応させる

**viewport 設定**

- `<meta name="viewport" content="width=device-width, initial-scale=1">`

**メディアクエリー設定方法は３種類**

- CSS に直接記述。 `@media (max-width: 700px) { … }`
- メディアクエリーで読み込む CSS を分ける。
  ```html
  <link rel="stylesheet" href="style.css" />
  <!-- 上に加え、下で指定した幅ではそれも読み込む -->
  <link rel="stylesheet" href="desktop.css" media="min-width:701px" />
  <link rel="stylesheet" href="mobile.css" media="max-width:700px" />
  ```
- `@import` で読み込む (@import は他より読み込みが遅いので非推奨)
  ```css
  @charset 'UTF-8';
  @import url('mobile.css') (maw-width: 700px);
  ```

#### c304 各要素を装飾する

- border-radius で楕円  
  `border-radius: (横の半径) 左上 右上 右下 左下 / (縦の半径) 左上 右上 右下 左下;`

  - 各頂点の丸みの値 `横の半径 / 縦の半径` と指定すると楕円の円弧をベースにした角丸を実装出来る。
  - 半径の値が一致するなら省略出来る。(縦半径は全一致だから一つだけ書くなど)
  - レスポンシブに対応するなら % 指定。

- テキストを円形に画像に回り込ませる  
  円形画像を囲ったクラスに `shape-outside: circle(); float: left;` を指定する。

- ボタンの装飾  
  `box-shadow: 横影の位置 縦影の位置 ぼかし 影の大きさ 影の色`
  ```css
  .btn a {
  	box-shadow: 0 0 0 5px #eda1a1 /* ボカシなしで影同色 */
  	border: 2px dashed #e38787; /* 縫い目風 */
  	border-radius: 5px;
  }
  ```

#### c306 各要素を装飾する(枠・ページ送り)

- blockquote タグ ブロック引用要素で引用文のｐタグを囲む。

#### 囲み枠の装飾

- 二重線の幅は outline-offset の値で指定する。

#### c308 スクロールに合わせて追従させる

`position: sticky;` スクロールで要素を固定する

#### c402 枠からはみ出す要素を作る方法

- 背景画像の一括指定

`background: url('images/bg-hero.jpg') no-repeat right top / 70vw auto;`

- 個別指定

```css
background-image: url('images/bg-hero.jpg');
background-repeat: no-repeat;
background-position: right top;
background-size: 70vw auto;
```

c403 グラフ例

c404 画像テキスト交互表示

c405 表で表示

c406 タイムラインを表示

c407 フォームの装飾

c408 属性セレクタ `コミットメッセ修正`

### c5 LP の作り方とアニメーション

#### c502 CSS でページ内をスルスル動かす

ページ内リンクの移動をスルスルと動くエフェクトにする。

```CSS
html {
  scroll-behavior: smooth;
}
```

ヘッダー固定表示

```css
header {
  position: fixed;
  width: 100%;
  z-index: 1;
}
```

c503 ブレンドモードで画像の色を変える

#### c504 カスタムプロパティ(変数)を使う

- `:root` は CSS の擬似クラスで `<html>` 要素を表す。
- `:root` に定義するとどの位置からでも参照でき、カスタムプロパティの宣言などで使われる。
- カスタムプロパティ名定義は `--プロパティ名: 値;`
- カスタムプロパティの呼び出しは `color: var(--プロパティ名);`
- 大文字小文字は区別される。

#### c505 CSS でアニメーションをつける(トランジション)

トランジションは、

- 始点終点の２点間の装飾の変化を設定する。
- ホバーなどトリガーが必要。

#### c506 CSS でアニメーションをつける(キーフレーム)

- 開始から終了の間に経過地点を追加でき異なる装飾を加えられる。

c507 斜めのラインのデザインを作る

c508 グラデーションで表現する

c509 スライドメニューを設置する

### c6 ギャラリーサイトで学ぶ 動画と画像の使い方

c602 背景に動画を設置する

c603 画像をレスポンシブに対応させる

c604 マルチカラムでレイアウトを作る１

c605 マルチカラムでレイアウトを作る２

c606 フィルターで画像の色を変える

c607 カーソルを合わせると画像を拡大する

c608 要素に影をつける

- box-shadow と drop-shadow の比較。

c609 ライトボックスで画面いっぱいに表示する

c610 アニメーションを加える

c611 ダークモードに対応させる

c612 練習問題

### c7 HTML CSS 管理方法

c702 calc 関数で計算式を書く

c703 Sass を使って効率を上げる

#### c704 VSCode で Sass を利用する

- VSCode 拡張機能 DartJS Sass Compiler and Sass Watcher で scss ファイルを保存する度に css と css.map と２つの min ファイルに変換する。

#### c705 ネストを使いこなす

- ネスト例 親セレクター、クラス名、プロパティ

#### c706 パーシャルでファイルを分割する

- パーシャル 分割ファイルの事。ファイル名頭にアンスコをつける。
- 分割ファイルが多くなったらフォルダを分けて管理。

#### c707 スタイルを使いまわせる Mixin

- `@mixin スタイル名` でスタイルを定義して `@include スタイル名` で使い回す。
