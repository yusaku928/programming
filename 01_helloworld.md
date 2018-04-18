# 第1章 プログラムを作ろう！

辻真吾『Pythonスタートブック』（技術評論社, 増補改訂版, 2018）の第1章「プログラムを作ろう！」を，問題を解きながら読んでいく。

## 1.2 プログラミング言語Python

### なぜPythonなのか？

#### 有名な言語（一部）

* マシン語，アセンブラ，C，C++
* Objective-C，Java，C#
* Lisp，Mathematica
* Fortran
* COBOL
* Perl，Ruby，Python
* JavaScript
* SQL
* Prolog

#### 言語の評価軸

* 言語の表現力（少しのコードでたくさんのことができると高い。低いと小回りがきく。）
* ライブラリの充実度

**問題** Pythonはどうか。

## 1.3 Pythonのインストール

この講義では，しばらくはPythonをインストールせず，[Google Colaboratory](https://research.google.com/colaboratory/)を使う。ノートブックの保存方法を確認してから先に進むこと。（Google Colaboratoryには，[Chrome](https://www.google.co.jp/chrome/)でアクセスすることを推奨する．）

メモ：Python 2とPython 3

## 1.4 コンピュータに指示を出す

**問題** GUIとCUIの例を一つずつ挙げよ。

## 1.5 インタラクティブシェルではじめるPython

**問題** 次の計算結果をPythonで得る方法を述べよ。

* 2＋2
* 2×3
* 10÷4
* 10を3で割った商
* 10を3で割った余り
* 2の10乗（2^10と書くことが多い）

**問題** `abc`と`'abc'`の**評価結果**を比べよ。

**問題** `'あいうえお'`と`print('あいうえお')`の評価結果を比べよ。

**問題** 次の**スクリプト**は何をするものか。

```python
import random
random.choice([1, 2, 3, 4, 5])
```

補足

* 上のスクリプトの`random`は**モジュール**である。
* `[1, 2, 3, 4, 5]`のように，角括弧の中にデータを並べたものを**リスト**と呼ぶ。

## 1.6 はじめてのプログラムを書く

**問題** 次の**スクリプト**は何をするものか。

```python
import random                     #モジュールの読み込み
data = ['goo','choki','pa']       #リストの作成
data_choice = random.choice(data) #ランダム選択
print(data_choice)                #結果の表示
```
