# Private Access Portal Site

GitHubアップロード用の静的サイト一式です。

## 構成

- `index.html` - トップページ本体
- `assets/generated/` - 各パネル画像
- `assets/audio/` - BADCAT のMP3
- `assets/logo/` - 左上ロゴ、ファビコン、Apple touch icon

## アップロード方法

このフォルダ内の `index.html` と `assets` フォルダを、GitHubリポジトリのルートに配置してください。

## 外部リンク設定

各パネルの外部リンク先は `index.html` 内の `panelLinks` に設定します。
空欄のままなら、そのパネルは遷移しません。

```js
const panelLinks = {
  spacex: "",
  viaiphone: "",
  rootsx: "",
  badcat: "",
  nfcgate: "",
  future: "",
};
```

例:

```js
const panelLinks = {
  spacex: "https://example.com/spacex",
  viaiphone: "https://example.com/viaiphone",
  rootsx: "https://example.com/rootsx",
  badcat: "https://example.com/badcat",
  nfcgate: "https://example.com/nfcgate",
  future: "https://example.com/future",
};
```

BADCAT の再生ボタンは、パネルリンクとは別に動作します。

## 注意

- `index.html` と `assets` の相対位置は変えないでください。
- このサイトは静的HTMLなので、WordPressテーマではありません。
- 旧サイト由来のリンクは無効化し、トップページのパネルだけ外部リンク設定できる構成にしています。
- GitHub Pages / Vercel / Netlify などの静的ホスティングで公開できます。
