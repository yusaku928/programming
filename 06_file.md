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
1. 「このファイルの種類には拡張機能'Python'が推奨されます。」と言われたら，「インストール」をクリックする。
1. 左下の「Select Python Environment」をクリックし，Anacondaを選択する。
1. `rand.py`の内容を以下のとおりとし，保存する。（途中でコード補完機能が働くことを確認する。）

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

## 標準入力

### 1行ずつ読み込む

**問題** Pythonで標準入力を処理する方法を，以下のプログラムtest.pyで確認せよ。（動作確認は`python rand.py | python test.py`でよい。）

```python
import sys

for line in sys.stdin:
    tmp = line.strip()#改行を除去
    print('[' + tmp + ']')
```

**問題** `python rand.py | python test2.py`とすると，rand.pyの出力を10倍した結果を表示するようなプログラムを書け。ヒント：`float(文字列)`とすれば,文字列が数値に変換される。

**問題** `python rand.py | python sum.py`とすると，rand.pyの出力を表示し，最後に数の合計を表示するプログラムを書け。

### まとめて読み込む

**問題** 次のプログラムhist.pyを，`python rand.py | python hist.py`のように使った場合の結果を調べよ。

```python
import sys
import matplotlib.pyplot as plt

step1 = sys.stdin.readlines()
step2 = list(map(float, step1))
plt.hist(step2)
plt.show()
```

**問題（オプショナル）** 「まとめて読み込む」方法を使うように，先のtest.pyを書き直せ。

**問題（オプショナル）** 「まとめて読み込む」方法を使うように，先のtest2.pyを書き直せ。

**問題（オプショナル）** 「まとめて読み込む」方法を使うように，先のsum.pyを書き直せ。

**問題（オプショナル）** 「1行ずつ読み込む」方法を使うように，先のhist.pyを書き直せ。

**問題（オプショナル）** 「0以上1未満の乱数10個の和」を1000個（1行に1個，つまり1000行）出力するプログラムrand2.pyを作り，`python rand2.py | python hist.py`を試せ。

### CSVファイルの処理

**問題** テキストエディタで次のような内容のtest.csvを作り，Excelで開いてみよ。

```
1,2,3,4
5,6,7
8,9
10
```

**問題** 文字列`line`に対して，`line.split(',')`とすると，カンマで分割した結果のリストが得られることを，次のコードで確認せよ。

```python
line = '1,2,3,4'
result = line.split(',')
print(result)
```

**問題** 数値をカンマで区切って並べた文字列`line`があるとき，そこに書かれた数値の合計が，次のコードで得られることを確認せよ。ヒント：`from statistics import *`とすると，リストの合計を求める関数`sum()`を使えるようになる。

```python
from statistics import *

line = '1,2,3,4'
tmp = map(float, line.split(','))#文字列を数値に変換する。
print(sum(tmp))
```

**問題** CSV形式のデータを標準入力から読み込み，1行ごとに，数の合計を出力するプログラムを書き，先に作成したtest.csvで動作を確認せよ。ファイルのデータはすべて数値だと仮定してよい。

## ファイル入力

**問題（オプショナル）** 先の問題は，次のようなプログラムでも解決できることを確認せよ。ファイルからの読み込みは標準入力を使うのが簡単だが，標準入力を使えない状況や，複数のファイルを使いたい場合には，このようなファイル入力を使う。

```python
from statistics import *

with open('test.csv', 'r') as myFile:
    for line in myFile:
        tmp = map(int, line.split(','))
        print(sum(tmp))
```

## ファイル出力

Pythonからファイルに出力したい場合は，リダイレクトを使えばよい。（例：`python test.py > result.txt`）

リダイレクトを使えない状況や，出力したいファイルが複数ある場合には，ファイル出力を使う。

**問題（オプショナル）** 次のコードの`'a'`を`'w'`に変えるとプログラムの振る舞いはどのように変わるか調べよ。

```python
with open('test.csv', 'a') as myFile:
  myFile.write('100,200,300\n')
  myFile.write('400,500\n')
```