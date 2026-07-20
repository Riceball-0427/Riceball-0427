# GitHub プロフィール設定手順ガイド

このディレクトリには、就活ポートフォリオとして機能する高品質な GitHub プロフィール README と、自動更新を行う GitHub Actions ワークフローが作成されています。
以下の手順に沿って、ご自身の GitHub アカウントに反映させてください。

---

## 1. リポジトリの準備

1. **GitHub 上でリポジトリを作成します：**
   - リポジトリ名：`Riceball-0427` （※ユーザー名と**完全に一致**させてください）
   - 公開設定：**Public** (公開)
   - 「Add a README file」は**チェックを入れずに**作成します。

2. **ローカルからプッシュします：**
   コマンドプロンプトまたは PowerShell を起動し、このフォルダ (`github-profile`) で以下のコマンドを実行します。
   ```bash
   git init
   git checkout -b main
   git add .
   git commit -m "Initial commit: professional profile setup"
   git remote add origin https://github.com/Riceball-0427/Riceball-0427.git
   git push -u origin main
   ```

---

## 2. GitHub リポジトリの権限設定 (超重要)

GitHub Actions が自動生成したグラフやスネークゲームの画像をリポジトリに保存（プッシュ）できるようにするため、書き込み権限を与える必要があります。

1. 作成したリポジトリ (`Riceball-0427/Riceball-0427`) のページを開きます。
2. 上部メニューの **Settings** (設定) タブをクリックします。
3. 左サイドバーの **Actions** > **General** を選択します。
4. 一番下までスクロールし、**Workflow permissions** セクションを探します。
5. **「Read and write permissions」** にチェックを入れて、**Save** をクリックします。

---

## 3. プライベートリポジトリの統計情報を含める場合 (任意)

デフォルトでは、公開されているパブリックリポジトリのデータのみがグラフやメトリクスに集計されます。ご自身のプライベートリポジトリの開発量も含めたい場合は、以下の設定を行ってください。

1. **Personal Access Token (PAT) の作成：**
   - GitHub 右上アイコン > **Settings** > 左サイドバー最下部 **Developer Settings** > **Personal access tokens** > **Tokens (classic)** を開きます。
   - **Generate new token (classic)** をクリック。
   - **Note** に `PROFILE_METRICS_TOKEN` などを入力。
   - **Expiration** (有効期限) を `No expiration` または長めに設定。
   - **Select scopes** で **`repo`** (リポジトリ全体へのアクセス権) にチェックを入れます。
   - 画面最下部の **Generate token** をクリックし、表示されたトークン文字列をコピーします（※一度画面を閉じると再表示されません）。

2. **リポジトリへのシークレット追加：**
   - プロフィールリポジトリ (`Riceball-0427/Riceball-0427`) > **Settings** > **Secrets and variables** > **Actions** を開きます。
   - **New repository secret** をクリック。
   - Name に **`PERSONAL_ACCESS_TOKEN`** と入力。
   - Secret に先ほどコピーしたトークン文字列を貼り付け、**Add secret** をクリックします。

3. **ワークフローファイルの修正：**
   - `.github/workflows/profile-3d.yml` と `metrics.yml` に記載されている `GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}` を、`token: ${{ secrets.PERSONAL_ACCESS_TOKEN }}` または `GITHUB_TOKEN: ${{ secrets.PERSONAL_ACCESS_TOKEN }}` に変更し、プッシュします。

---

## 4. 動作確認と初期実行

設定が完了したら、GitHub Actions を手動で実行して動作を確認します。

1. リポジトリの **Actions** タブをクリックします。
2. 左メニューから以下の各ワークフローを選択します：
   - **Generate 3D Contribution Graph**
   - **Generate Contribution Snake**
   - **GitHub Metrics**
3. 右側にある **Run workflow** ボタンをクリックし、手動で実行を開始します。
4. 数分で完了し、リポジトリ内に `profile-3d-contrib` フォルダや `output` フォルダ、そしてスネークゲーム用の `output` ブランチが自動生成されます。
5. ご自身のプロフィールトップページ (`https://github.com/Riceball-0427`) を開き、美しく装飾されたプロフィールが表示されていることを確認してください！
