# テーマ
CodeDeployで遊ぶ

---

# 実現できたこと

* サンプルアプリケーションの作成(ほぼチュートリアルと同じ)
* アプリケーション用githubリポジトリを作成してpush
* githubとcircleciを連携させた
* circleciでアプリケーションをzipに固めてS3へsync

▼これは失敗した・・・
* CodeDeployでS3においたアプリケーションをデプロイ(手動)

---

# やりたかったこと

* 正しくデプロイ可能な形でS3にアップしたかった
* CodeDeployでアプリケーション・デプロイグループなどを手で作成したが、これらをCloudFormaionにやらせたかった
