# Todo（iPhone用Webアプリ）

## 含まれるもの
- SwiftUI版の配色・丘と太陽のバナーを再現した画面
- Todo追加・編集・削除、期限、完了チェック
- 日付移動、完了履歴、進捗表示
- localStorageへの自動保存
- PWA設定とオフラインキャッシュ

## iPhoneで使う手順
1. このフォルダの中身をHTTPS対応の静的ホスティングへ公開します（例：GitHub Pages）。
2. iPhoneのSafariで公開URLを開きます。
3. 共有ボタン →「ホーム画面に追加」→「追加」。
4. ホーム画面のTodoアイコンから起動します。

## GitHub Pagesで無料公開する場合
1. GitHubにログインし、新しいPublicリポジトリを作成します。
2. `index.html`、`manifest.webmanifest`、`sw.js`、`icon-192.png`、`icon-512.png`をリポジトリ直下へアップロードします。
3. Settings → Pages → Deploy from a branch → `main` / `root` → Save。
4. 公開されたURLをiPhoneのSafariで開きます。

## データについて
TodoはそのiPhoneのSafari/Webアプリ領域（localStorage）に保存されます。別端末には同期されません。SafariのWebサイトデータ削除、端末故障・紛失、ブラウザ領域の初期化などで消える可能性があるため、重要なデータは定期的にバックアップしてください。

## 補足
Webアプリはネイティブアプリではないため、SwiftUIの触覚フィードバックや一部のOS固有挙動は完全一致しません。ホーム画面追加・オフライン利用にはHTTPSでの公開が必要です。
