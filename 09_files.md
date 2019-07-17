# ファイル

## 準備

1. [Google Colaboratory](https://research.google.com/colaboratory/)で「Python 3の新しいノートブック」を作る．
1. ノートブックの名前を「09」に変える．

## 演習

**問題** テキストをファイルに書き出す方法を確認せよ。

```python
with open('test.txt', 'w', encoding='utf-8') as my_file:
  my_file.write('こんにちは')
```

```
# ファイルができていることの確認
!ls
```

**問題** ファイルからテキストを読み込む方法を確認せよ。

```python
with open('test.txt', 'r', encoding='utf-8') as my_file:
  print(my_file.read())
```

**問題** 1以上10以下の整数を，1行に1個ずつファイルtest.datに書き出せ。

**問題** test.datの内容を画面に表示するPythonプログラムを書け。

```
# 想定していない回答
!cat test.dat
```

**問題** 次のような内容のファイルtest.csvをPythonで作れ。

```
1,10,100
2,20,200
（省略）
10,100,1000
```

```python
# ファイルの確認
!cat test.csv
```

**問題** test.csvを読み，行ごとの合計値を画面に表示せよ。

ヒント：リストの要素の合計は次のように求められる。

```python
foo = [1, 2, 3, 4]
print(sum(foo))

bar = ['1', '2', '3', '4']
baz = [int(i) for i in bar]
print(sum(baz))
```

**問題（レポート課題）** 上の問題をPandasというライブラリを使って解決せよ。（こういう話は後期の「データマイニング入門」で詳説する。） 

```
import pandas as pd
df = pd.read_csv('test.csv', header=None)
# あと1行必要
```

**問題（レポート課題）** test.csvを読み，列ごとの合計値を画面に表示せよ。
