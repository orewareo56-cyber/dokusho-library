# 読書中毒計画

読書習慣を整えるための静的Webページです。GitHub Pagesで公開できるよう、`index.html` を公開入口として構成しています。

## ローカル確認方法

このフォルダで簡易サーバーを起動して確認します。

```sh
python3 -m http.server 8000
```

ブラウザで以下を開きます。

```text
http://localhost:8000/
```

HTMLファイルを直接開くこともできますが、GitHub Pages公開時に近い動作を確認するにはローカルサーバー経由がおすすめです。

## GitHub Pages公開手順

1. このフォルダをGitリポジトリにします。

```sh
git init
git add .
git commit -m "Prepare static site for GitHub Pages"
```

2. GitHubで新規リポジトリを作成します。
3. GitHubに表示される案内に従ってリモートを追加し、`main` ブランチへpushします。

```sh
git branch -M main
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main
```

4. GitHubのリポジトリ画面で `Settings` → `Pages` を開きます。
5. `Build and deployment` の `Source` を `Deploy from a branch` にします。
6. `Branch` を `main`、フォルダを `/ (root)` にして保存します。
7. 数分後に表示される公開URLへアクセスします。

## 更新手順

変更後はローカルで表示確認し、問題なければcommitしてpushします。

```sh
git status
git add .
git commit -m "Update reading plan page"
git push
```

GitHub Pagesにはpush後しばらくして自動反映されます。スマホで確認する場合は、ブラウザの再読み込みやキャッシュ削除が必要になることがあります。
