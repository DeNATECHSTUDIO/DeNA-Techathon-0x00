PHPのマイクロフレームワークである「Slim」を使って、簡単な匿名型QAサイトを作りました。

# 実施したこと
- ローカルのMac上にvagrantでLinuxサーバを構築。
- Ansibleで必要なソフトウェア（PHP、Redis）を導入。
- PHPのcomposerを使って、Slimフレームワークの雛形を導入。
- 実装。フロントはbootstrapを使用。永続データの保持はRedisを使用。

# 実施できなかったこと
- 見た目のブラッシュアップ
- 管理者機能（不適切な書き込みを削除する機能等）
- セキュリティ対策
- 外部への公開

# 関連リンク
[Slim](https://www.slimframework.com/)

[リポジトリ](https://github.com/bassbone/slim-qasite)
