# Private Access Portal Site

GitHubアップロード用の静的サイト一式です。

## 構成

- `index.html` - トップページ本体
- `assets/generated/` - 各パネル画像、パネル内ロゴ
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
  nfcgate: "https://nfcgate.jp/",
  future: "",
};
```

現在リンクが有効なのは `NFC GATE` のみです。
BADCAT の再生ボタンは、パネルリンクとは別に動作します。

## 注意

- `index.html` と `assets` の相対位置は変えないでください。
- このサイトは静的HTMLなので、WordPressテーマではありません。
- GitHub Pages / Vercel / Netlify などの静的ホスティングで公開できます。
