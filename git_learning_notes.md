### GitとGitHubの学び：超要約ノート

-----

#### 1\. GitとGitHubの基本

  * **Git**: ファイルの変更履歴をPC内で管理するシステム。
  * **GitHub**: Gitリポジトリをインターネット上で共有・保存するサービス。
  * **ローカルリポジトリ**: あなたのPC上のGit管理フォルダ。
  * **リモートリポジトリ**: GitHub上のGit管理場所。

#### 2\. 学習フォルダをGitHubにアップロードする手順

1.  **ローカルリポジトリの準備**:

      * `techschool-curriculum`フォルダに移動: `cd /path/to/your/techschool-curriculum`
      * Gitを初期化（初回のみ）: `git init`
      * `3-9`フォルダをコピー: `cp -r /Users/nishishimahiroshi/HTML_CSS/3-9 .`
      * 変更をステージング: `git add .` (または `git add 3-9`)
      * 変更をコミット: `git commit -m "コミットメッセージ"`

2.  **GitHubとの接続設定**:

      * **GitHubで空のリポジトリを作成**: ウェブサイトで`techschool-curriculum`という名前で新規作成（READMEなどは**チェックしない**）。
      * ローカルとGitHubを紐付け: `git remote add origin https://github.com/Hiroshift/techschool-curriculum.git`
      * ブランチ名を`main`に設定: `git branch -M main`

3.  **GitHubへのプッシュ（アップロード）**:

      * プッシュ実行: `git push -u origin main`
      * **認証**:
          * `Username:` に**GitHubユーザー名**を入力。
          * `Password:` に**Personal Access Token (PAT)** を入力。（入力は表示されない）

#### 3\. トラブルシューティング（重要！）

  * **`'origin' does not appear to be a git repository` エラー**:

      * 原因: `git remote add origin ...` が未実行か、URL間違い。
      * 解決: 上記「GitHubとの接続設定」の手順を再確認・実行。

  * **`Support for password authentication was removed` エラー**:

      * 原因: GitHubがパスワード認証を廃止したため。
      * 解決: **Personal Access Token (PAT)** を使う。
          * **PAT発行手順**:
            1.  GitHubログイン → プロフィールアイコン → `Settings` (アカウント全体の設定)
            2.  左メニューの `Developer settings` または `Access` セクション内の `Personal access tokens` → `Tokens (classic)`
            3.  `Generate new token (classic)` をクリック。
            4.  `Note` (名前)、`Expiration` (期限)、`repo`スコープにチェック。
            5.  生成された**トークン文字列を必ずコピーして控える**（再表示されない）。
            6.  `git push`時に、パスワードとしてこのPATを入力する。

#### 4\. 今後のGit操作の基本

  * 変更後: `git add .` → `git commit -m "変更内容"` → `git push origin main`
  * 履歴確認: `git log`
  * 状態確認: `git status`