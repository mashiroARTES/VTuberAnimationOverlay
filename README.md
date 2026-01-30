📺 VTuberAnimationOverlay for OBS (Firebase Cloud Sync 版)

このプロジェクトは、Firebase Realtime Databaseを利用して、OBS上のオーバーレイをブラウザからリアルタイムに書き換えることができるツールです。 URLに固有の id を含めることで、複数の配信者がそれぞれ自分専用の設定を保持・運用できます。

🔗 クイックリンク
ベースURL: https://mashiroartes.github.io/VTuberAnimationOverlay/index.html

🚀 使い方
1. 自分専用のIDを決める
他のユーザーと重複しない、自分専用のID（英数字）を決めてください。

例：my_stream_01 など

2. 配信画面（OBS）への追加
OBSのソース一覧から「ブラウザ」ソースを新規作成します。

URL欄に以下のように自分のIDを付け加えたURLを入力します。 https://mashiroartes.github.io/VTuberAnimationOverlay/index.html?id=【自分のID】

幅を 1920、高さを 1080 に設定してください。

3. 内容の編集（エディター画面）
通常のブラウザ（Chrome等）で、URLの末尾に &edit を付けた状態で開きます。 https://mashiroartes.github.io/VTuberAnimationOverlay/index.html?id=【自分のID】&edit

画面上のエディターで「テーマカラー」「各項目のタイトル」「内容」を入力します。

「クラウドに保存・即時反映」**ボタンを押すと、OBS側の画面がリロードなしで瞬時に切り替わります。

🛠 セットアップ（開発者向け）
自分でFirebaseを管理・ホストする場合は、以下の手順を行ってください。

Firebaseの設定:

Firebase Console でプロジェクトを作成。

Realtime Database を有効化。

index.html 内の firebaseConfig 変数を、自身のプロジェクト設定に書き換えてください。

GitHub Pagesへのデプロイ:

リポジトリの Settings > Pages から公開設定を行ってください。

⚠️ セキュリティと注意点
IDの秘匿: ?id=...&edit を含むURLは、あなたのオーバーレイを操作するための鍵となります。配信画面に映したり、他人に教えたりしないでください。

推測されにくいID: id=test などの簡単な文字列は第三者に上書きされる可能性があるため、ランダムな英数字を組み合わせたIDの使用を推奨します。

データ保持: Firebaseの無料枠内で動作しますが、長期間アクセスがない場合や設定によってはデータが削除される可能性があります。重要な設定はメモしておくことをお勧めします。

🛠 トラブルシューティング（動かない場合）
もし設定が反映されない場合は、以下の点を確認してください。

IDが入力されているか: URLの末尾に ?id=xxx が正しく入っているか確認してください。

Firebaseのリージョン: このプロジェクトは asia-southeast1 (シンガポール/日本近隣) リージョンを使用しています。自分でFirebaseを立て直す場合は、databaseURL のドメインが一致しているか確認してください。

OBSのキャッシュ: 設定を変更したのにOBSが変わらない場合は、OBS側のブラウザソースプロパティにある「現在のページのキャッシュを更新」ボタンを押してください。

📄 ライセンス
MIT License ご自身の配信スタイルに合わせて自由にカスタマイズしてご活用ください。
