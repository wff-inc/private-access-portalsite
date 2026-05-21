# SYNAPSE Static Site

SYNAPSE向けの静的WEBサイトです。新聞紙面風のビジュアルレイアウトをベースに、SpaceX Private Access、The One、RootsX Exchange、Future Lifestyle Store、NFCGATEなどのコンテンツを1ページにまとめています。

## 概要

このリポジトリは、サーバーへそのまま配置して公開できる静的サイト一式を管理するためのものです。主要なページは `index.html` に含まれており、画像・CSS・フォントなどの必要アセットも同梱されています。

| 項目 | 内容 |
|---|---|
| サイト種別 | 静的WEBサイト |
| メインファイル | `index.html` |
| 主要画像 | `assets/generated/` |
| ベースCSS | `wp-content/themes/seaharvest/dist/css/screen.css` |
| フォント・補助画像 | `wp-content/themes/seaharvest/fonts/`, `wp-content/themes/seaharvest/img/` |

## ディレクトリ構成

```text
.
├── index.html
├── assets/
│   └── generated/
│       ├── spacex-private-access.png
│       ├── the-one-piano.png
│       ├── rootsx-exchange.png
│       ├── future-lifestyle-store.png
│       └── nfcgate-access.png
└── wp-content/
    └── themes/
        └── seaharvest/
            ├── dist/css/screen.css
            ├── fonts/
            └── img/
```

## ローカル確認方法

任意のローカルサーバーで確認できます。Pythonが利用できる環境では、以下のコマンドで簡易サーバーを起動できます。

```bash
python3 -m http.server 8787
```

起動後、ブラウザで次のURLへアクセスします。

```text
http://127.0.0.1:8787/index.html
```

## 公開方法

`index.html`、`assets/`、`wp-content/` を同じ階層に保ったまま、サーバーの公開ディレクトリへアップロードしてください。

```text
public_html/
├── index.html
├── assets/
└── wp-content/
```

## 注意事項

このサイトは静的HTMLとして納品されているため、WordPress本体やデータベースは含まれていません。外部サーバーへ配置する場合は、画像・CSS・フォントへの相対パスが維持されるようにしてください。
