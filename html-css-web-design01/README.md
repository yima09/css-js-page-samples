### 1 冊ですべて身につく HTML & CSS と Web デザイン入門講座 Mana

#### c1-7 制作の流れ

企画 - サイトマップ制作 - ワイヤーフレーム制作 - デザイン - コーディング - 公開

- サイトマップは２〜３階層におさめる。
- 優先順位の高いページをナビメニューに配置。

- ワイヤーフレームはファーストビューに何を伝える目的のサイトなのか優先順位を付けてレイアウトを組む。視線の動きは左上からなど。

- 公開時にファイル数が多い場合 FTP (ファイル転送) ソフトを使う。

#### c2-3 HTML ファイルの骨組み

`<!doctype html>` や html, head, meta, body などの解説。

#### c2-5 見出しをつけよう

大見出しの h1 は基本的には１つの Web ページにつき一度の利用が良いとされる。

#### c2-8 リンクを貼ろう

a タグで囲まれた要素がリンクになる。

`<a href="mailto:info@example.com">お問い合わせ</a>` とするとクリックされた際にメールアプリが立ち上がり送信先に指定のアドレスが入力された状態になる。

#### c2-12 より使いやすいフォームにしよう

`<input type="checkbox">` の id 属性と label タグの for 属性の値を一致させるとラベル部分でもチェックできるようになる。

#### c2-13 ブロック要素でグループ分けをしよう

- header ヘッダー。
- nav タグはナビゲーションメニュー。
- article は読み物、記事、そこだけで独立したページとして成り立つような内容。
- section ひとかたまりごとのテーマでまとめる。
- main メインとなる部分でその中に article や sections などが入れる。
- article メインコンテンツではない補足情報。
- footer フッター。
- div 上記に当てはまらない、デザインのためだけなどのタグ。

#### c3-2 CSS を適用させる方法

- head タグに link タグで指定。一括管理。
- head タグに style タグでそこに CSS を書く。記述ファイルのみ適用。
- タグ の style 属性でそこに CSS を書く。 記述タグのみに適用。優先度は高く上記を上書きする。

#### c3-4 CSS の基本の書き方を身につけよう

- `セレクター { プロパティ: 値; }`
- px は絶対値、 rem, % は相対値

#### c3-5 文字や文章を装飾しよう

- font-size は数値単位の他にキーワード７段階も指定できる。
- 文字サイズは 14px ~ 18px, バリエーションは２〜５種類程度に設定。
- 文字のジャンプ率は高いと躍動的、低いと落ち着いた雰囲気。
- フォントは１〜３種類。
- line-height の単位なし数値はフォントサイズとの比率で 1.5 ~ 1.9 で調整する。

#### c3-8 背景を彩ろう

#### c3-12 リストを装飾しよう

- list-style-type リストマーカーの種類
- list-style-position リストマーカーの位置(外側か内側)
- list-style-image マーカーの画像

#### ページ内リンク

```html
<a href="#contents">クリックすると移動</a>

<div id="contents">
  <p>移動先はここ</p>
</div>
```

#### c3-14 レイアウトを組もう Flexbox

#### c3-14 レイアウトを組もう Grid

### c4 フルスクリーンの Web サイトを再索する

#### c4-7 フルスクリーンページのカスタマイズ例

```css
/* 青色系にカスタマイズ例 */
#home {
  background-image: url(../images/main-bg.jpg);
  background-color: #0bd;
  background-blend-mode: hard-light;
  min-height: 100vh;
}
```

```css
/* 背景をグラデーションカラーにカスタマイズ例 */
#home {
  background-image: url(../images/main-bg.jpg), linear-gradient(#c9ffbf, #ffafbd);
  background-blend-mode: luminosity;
  min-height: 100vh;
}
```

### c5 ２カラムの Web サイトを制作する

#### c5-9 カラムページのカスタマイズ例

- ３カラムのレイアウト設定

### c6 タイル型レイアウトとは

#### c6-5 レスポンシブに対応させよう

```css
.grid {
  /* grid-template-columns: 1fr 1fr 1fr; */
  /* 1. 値を `repeat(繰り返す数, 要素の幅)` で書き直す */
  /* grid-template-columns: repeat(3, 1fr); */
  /* 2. minmax(最小, 最大) で画像幅の最小最大値を指定する */
  /* grid-template-columns: repeat(3, minmax(240px, 1fr)); */
  /* 3. ３つ並び指定で幅が小さいと見切れるので auto-fit で折り返す */
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
}
```

### c7 外部メディアを使用する

#### c7-08 OGP の設定を使用

- OGP 「Open Graph Protocol」

#### c7-09 外部メディアのカスタマイズ例

- Google マップの表示カスタマイズ例
