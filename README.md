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

