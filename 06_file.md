# 第6章 ファイルの読み書き

## Anaconda Promptでのファイル・フォルダ（ディレクトリ）操作

**問題** 以下のコマンドの意味と使い方を述べよ。

* c:
* cd
* mkdir
* dir
* ren
* del
* type
* more

Windowsのコマンドを極めたい人は，[Windows Commands Reference（英語約1000ページ）](https://www.microsoft.com/en-us/download/details.aspx?id=56846)を参照。

**問題** Anaconda Promptで`c:/cit/test1/test2`を作れ。

## Anaconda PromptでのPythonプログラムの実行

1. VSCodeで新しいファイルを作り，`rand.py`という名前で保存する。
1. Pythonのための拡張機能のインストールを促されるから，インストールする。
1. 左下の「Select Python Environment」をクリックし，Anacondaを選択する。
1. `rand.py`の内容を以下のとおりとし，保存する。

```python
import random

for i in range(100):
  x = random.randint(1, 1000)
  print('{0:4d}'.format(x))

```
Anaconda Promptで以下のように実行する。

```bash
c:
cd /cit
python rand.py
```

**問題** `rand.py`は何をするプログラムか。

## リダイレクトとパイプ

**問題** `rand.py`の実行結果を`result.txt`に書け。ヒント：**リダイレクト**を使う。

**問題** `rand.py`の実行結果を1画面ずつ閲覧する方法を述べよ。ヒント：**パイプ**を使う。

**問題** `rand.py`の実行結果を小さい順に並び替えよ。

**問題** `rand.py`の実行結果を大きい順に並び替えよ。

**問題** `rand.py`の実行結果を小さい順に並び替えた結果を`result2.txt`に書け。

**問題** `rand.py`の実行結果を大きい順に並び替えた結果を1画面ずつ閲覧する方法を述べよ。

**問題（オプショナル）** 数が小さい順に出力されるように，`rand.py`を修正せよ。
