### git_practice200906

# 始めてのGitHub
[Gitコマンド一覧 Qiita](https://qiita.com/fukumone/items/73e1a9a62c5e4454263b)
　
### Step1: リポジトリを作成
----------------
GitHubのページ左上の`New`を押します。

1.  **_Repository name_**を記入(_Description_は記入してもしなくてもいい)
2. **_Public_**を選択  
3.  **_initialize this repository with a README_** にチェックを入れて`Create repository`を押します

### Step2: リポジトリのクローン
--------------
1. **_clone or download_**→URLをコピーします。
2. **<span style="color: #069417">チームのリーダー</span>**はこのURLをメンバーに共有してください。
3. **<span style="color: #2357b5">メンバー全員</span>**は以下のコマンドを使用してリポジトリをクローン(複製)します。

```bash
# 作業ディレクトリに移動
$ cd 作業ディレクトリ
# リポジトリをクローン
$ git clone コピーしたURL(リポジトリのURL)
# cloneしたリポジトリの確認
$ ls
>workshop-repositry
$ cd workshop-repositry
# 中身の確認
$ ls
>README.md
```
### Step3: 作業ブランチを切り替える
----
`git branch`コマンドを打つことで、**現在のブランチ**(*がついているブランチ)を確認できます。
`git branch -a`コマンドを打つことで、**全てのブランチ**を確認できます。
```bash
#ブランチの確認
$ git branch -a
> * master
> remotes/origin/HEAD -> origin/master
> remotes/origin/master
```
`git log`コマンドを押すことで、コミット履歴の閲覧ができます。
現在は、リポジトリを作った直後なので、一つだけが表示されています。
```bash
$ git log
> commit beed01c8f93cdcf609c7f1064ebbc8d38b7809c3 (HEAD -> master, origin/master, origin/HEAD)
> Author: y-shoji <50990774+y-shoji@users.noreply.github.com>
> Date:   Sat Nov 23 14:24:41 2019 +0900
>
>     Initial commit
```

gitにはブランチルールがあります。このルールを守ることで、スムーズなチーム開発を行うことができます。

[Gitのブランチモデルについて ](https://qiita.com/fukumone/items/73e1a9a62c5e4454263b)

