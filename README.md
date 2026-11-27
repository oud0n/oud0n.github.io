# oud0n.github.io

アプリの製品案内・サポートページ・プライバシーポリシーの置き場。`https://oud0n.github.io/<アプリ>/` で公開される。

- `index.html`：アプリの一覧
- `assets/site.css`：全ページ共通の見た目
- `<アプリ>/index.html`：サポート（App Store Connect の「サポート URL」）
- `<アプリ>/privacy.html`：プライバシーポリシー（「プライバシーポリシー URL」）

## 製品案内

- `apps/laploupe/index.html`：LapLoupe の概要と、iPhone/iPad・Mac・Windows・ブラウザ版への入口。
- `apps/meishitrace/index.html`：MeishiTrace の概要と、App Store・既存サポートへの入口。
- `apps/<アプリ>/` は製品案内用。同名リポジトリの Pages と競合しない URL にする。
- `sitemap.xml`：サイトトップと製品ページ。`robots.txt` に発見用の URL を記載。
- 製品ページのタイトル・説明・canonical・OG の URL は公開先に合わせる。

### LapLoupe の配布リンク更新

PC の新しい安定版を公開したら、`apps/laploupe/index.html` の日本語・英語両方の版番号と dmg/exe の URL を更新する。リンクは `oud0n/ds_universal` の公開 Releases に実在する安定版の配布物と照合する。日本語・英語で Mac と Windows のリンク先・表示バージョンが一致することを確認する。旧配布物を使う場合も、最新リリースへのリンクは残す。

ローカル確認：`python3 -m http.server 8765 --bind 127.0.0.1` をこのディレクトリから起動し、`http://127.0.0.1:8765/` と `/apps/laploupe/` を開く。スマホ幅・ライト／ダークと、各配布先へのリンクを確認する。静的 HTML のためビルドは不要。
