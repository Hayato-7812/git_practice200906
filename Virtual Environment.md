# 仮想環境の作り方

## 開発環境
* Mac OS
* Flask,Visual Studio Code
* anaconda
* Python3.7


## 
1. 仮想環境の構築
ターミナルで以下のコマンドを実行

```bash
# flaskという仮想環境を作り、そこにpython3.7をインストール
~ $ conda create --n flask python=3.7
```
2. 仮想環境を有効化する
```bash 
# Flaskという名前の仮想環境を有効にする
~ $ source $PYENV_ROOT/versions/anaconda3-4.1.1/bin/activate flask
```
 追記：本来であれば`conda activete <環境名>`で仮想環境の起動ができるはずなのだが、  
     エラー分が出てしまったので今回は上記コマンドで対応
_* 参照: *_ [pyenvとanacondaを共存させる時のactivate衝突問題の回避策3種類 - Qiita](https://qiita.com/y__sama/items/f732bb7bec2bff355b69/)

3. 仮想環境を無効化する
```bash
# 仮想環境を無効化
~ $ conda deactivate
```
