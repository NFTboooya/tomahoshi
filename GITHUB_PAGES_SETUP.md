# GitHub Pagesセットアップ手順

このファイルは、退職手当計算アプリをGitHub Pagesで公開するための詳細な手順です。

## 📋 前提条件

- GitHubアカウント（無料）
- インターネット接続
- Webブラウザ

## 🚀 Step 1: GitHubアカウント作成（既にある場合はスキップ）

1. https://github.com/ にアクセス
2. 「Sign up」をクリック
3. メールアドレス、パスワード、ユーザー名を入力
4. メール認証を完了

## 📦 Step 2: 新しいリポジトリ作成

1. GitHubにログイン
2. 右上の「+」→「New repository」をクリック
3. 以下を入力:
   - **Repository name**: `retirement-calculator`（または任意の名前）
   - **Description**: `北海道教育職員の退職手当計算ツール`
   - **Public**: ✅ 選択（無料で公開）
   - **Add a README file**: ☑️ チェックを外す（既にREADME.mdがあるため）
4. 「Create repository」をクリック

## 📤 Step 3: ファイルのアップロード

### 方法A: Webインターフェース経由（簡単）

1. 作成したリポジトリのページで「uploading an existing file」をクリック
2. AI Driveから以下のファイルをダウンロード:
   - `index.html`（メインファイル）
   - `README.md`
   - `LICENSE`
   - `.gitignore`
   - `GITHUB_PAGES_SETUP.md`（このファイル）
3. すべてのファイルをドラッグ&ドロップ
4. 下部の「Commit changes」をクリック

### 方法B: Git CLI経由（上級者向け）

```bash
# ローカルでファイルをダウンロード後
git clone https://github.com/[ユーザー名]/retirement-calculator.git
cd retirement-calculator

# AI Driveからダウンロードしたファイルをコピー
# すべてのファイルをこのディレクトリに配置

git add .
git commit -m "初回コミット: 退職手当計算ツール v2.1"
git push origin main
```

## 🌐 Step 4: GitHub Pagesを有効化

1. リポジトリページで「Settings」タブをクリック
2. 左サイドバーの「Pages」をクリック
3. **Source**セクション:
   - **Branch**: `main` を選択
   - **Folder**: `/ (root)` を選択
4. 「Save」をクリック
5. 数分待つと、ページ上部に公開URLが表示されます:
   ```
   Your site is published at https://[ユーザー名].github.io/retirement-calculator/
   ```

## ✅ Step 5: 動作確認

1. 表示されたURLにアクセス
2. アプリが正常に表示されることを確認
3. 簡単な計算テストを実行

## 🔄 更新方法

ファイルを更新する場合:

1. リポジトリページで更新したいファイルをクリック
2. 右上の鉛筆アイコン（Edit）をクリック
3. 内容を編集
4. 「Commit changes」をクリック
5. 数分で変更が反映されます

## 🎯 完成！

公開URL:
```
https://[あなたのGitHubユーザー名].github.io/retirement-calculator/
```

このURLを同僚に共有してください！

## 📝 カスタムドメインの設定（オプション）

独自ドメイン（例: `taishoku.example.com`）を使いたい場合:

1. Settings → Pages → Custom domain に独自ドメインを入力
2. DNSレコードを設定（詳細はGitHubヘルプ参照）
3. 「Enforce HTTPS」にチェック

## ❓ トラブルシューティング

### ❌ 404 Not Found エラー
- GitHub Pagesの有効化後、数分待つ
- ブラウザのキャッシュをクリア（Ctrl+Shift+R）
- ファイル名が `index.html` であることを確認

### ❌ ファイルが表示されない
- すべてのファイルがルートディレクトリにあることを確認
- ファイル名の大文字小文字を確認

### ❌ 計算が動作しない
- ブラウザのコンソール（F12）でエラーを確認
- index.htmlが完全にアップロードされているか確認

## 📞 サポート

問題がある場合:
- [GitHub Pagesヘルプ](https://docs.github.com/ja/pages)
- [リポジトリのIssues](../../issues)で質問

---

**最終更新**: 2026年1月14日
