📺 VTuberAnimationOverlay for OBS (Firebase Cloud Sync 版)
このプロジェクトは、OBS用の動的なオーバーレイをクラウド（Firebase）経由で操作できるツールです。 エディター画面で保存ボタンを押すだけで、配信画面上のオーバーレイがリロードなしで即座に更新されます。

✨ 主な機能
リアルタイム同期: Firebase Realtime Database を使用し、秒速で内容を反映。

トピック編集: 3つの項目のタイトルと内容を自由に変更可能。

カラーカスタマイズ: 配信の雰囲気に合わせてメインカラーを一括変更。

モバイル対応: GitHub Pages にホストすれば、スマホからセトリ更新が可能。

🚀 使い方
1. 配信画面（OBS）への表示
https://mashiroARTES.github.io/VTuberAnimationOverlay/index.html をコピーします。

OBSのソースに「ブラウザソース」を追加し、上記のURLを貼り付けます。

幅を 1920、高さを 1080 に設定してください。

2. 設定の変更（エディター）
公開したURLの末尾に ?edit を追加してブラウザで開きます。

例: https://.../index.html?edit

内容やカラーを編集し、「クラウドに保存・反映」ボタンを押すと即座にOBS側に反映されます。

🛠 セットアップ（開発者向け）
Firebaseの準備

Firebase Console でプロジェクトを作成。

Realtime Database を作成（テストモード推奨）。

コードの書き換え

index.html 内の const firebaseConfig 部分を、自分のプロジェクト情報に書き換えてください。

GitHub Pages で公開

リポジトリの Settings > Pages から、main ブランチを公開ソースに設定。

⚠️ セキュリティに関する注意
エディターURLの管理: ?edit 付きのURLは管理者用です。配信画面に映したり、SNSで共有したりしないでください。（誰でも内容を書き換えられてしまうため）

Firebaseルール: 本格的に運用する場合は、Firebaseの「ルール」で書き込み制限をかけるか、APIキーにHTTPリファラー制限（GitHub Pagesのドメインのみ許可）をかけることを推奨します。

📄 ライセンス
MIT License - ご自由にカスタマイズして配信にご活用ください！
