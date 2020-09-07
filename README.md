### git_practice200906

# 始めてのGitHub
[Gitコマンド一覧 Qiita](https://qiita.com/fukumone/items/73e1a9a62c5e4454263b)
　
### 1. ローカルリポジトリ の作成
フォルダ（やその中身のファイル）を作成したらターミナルを開いてかのコマンドを実行
```badh
$ cd Desktop/intro_git
$ git init
>Reinitialized existing Git repository in /Users/shimizuhayato/Desktop/intro_git/.git/
```
### 2. リモートリポジトリ 準備
Git Hub にログインし画面左上の`New`をクリック
リポジトリ の名前等を入力し`Create repositry`をクリック

### 3. ローカルとリモートの接続
HTTPSのURLをコピー
ターミナルで以下のコマンドを実行
```bash
$ git remot add origin <URL>
```

#### リモートリポジトリ が既にある場合
`git clone`コマンドを使用

ターミナルでローカルリポジトリ を作成したいディレクトリーまで移動し、以下のコマンドを実行
```bash
$ git clone <URL>
```

## add,commit,push
1. `add`---->commitする内容の選択
2. `commit`->セーブポイントの作成
3. `add`---->ローカルリポジトリをリモートリポジトリに反映

# 覚えておくべきコマンド
[](最後の方につける)
gitの管理下から外す
ファイルの拡張子に　_**.gitignore**_をつける

1. ファイルへの変更の取り消し方(addする前の段階)
```bash
# ファイルの変更を取り消す
~ $ git checkout -- <ファイル名>

# ディレクトリの変更を取り消す
~ $ git checkout -- <ディレクトリ名>

# 全変更を取り消す
~ $ git checkout -- .

2. ステージした変更を取り消す(addの内容を取り消す/commitをステージに上書きする)

```bash
# ステージしたファイルの変更を取り消す 
~ $ git reset HEAD <ファイル名>

# ステージしたディレクトリの変更を取り消す
~ $ git reset HEAD <ディレクトリ名>

# ステージした全変更を取り消す
~ $ git reset HEAD .
```
3. 直前のコミットを変更する

```bash
# 直前のコミットを変更する
~ $ git commit --amend
```
_*注意*_
> リモートリポジトリ にpushしたものは変更できないので注意すること  
> pushしたものを変更するときは再度commitする

## リモートリポジトリとのやりとり

```bash
# 対応するリモートリポジトリを表示
~ $ git rmeote

# 対応するURLを表示
~ $ git remote -v

# リモートリポジトリの追加
~ $ git remote add <名前><URL>
# tutorialという名前でリモートリポジトリのURLを登録する
~ $ git remote add tutorial
https//githib.com/user/repo.git
```
### リモートリポジトリの情報を取得する
```bash 
# 方法1
# リモートリポジトリの情報を取得(ローカルリポジトリへ)
~ $ git fetch <名前>/<branch名>
~ $ git fetch origin
# ^での情報をワークツリーに反映する
~ $ git marge origin/master

# 方法2
# リモートリポジトリの情報を取得
~ $ git pull<名前>/<ブランチ名>
```
