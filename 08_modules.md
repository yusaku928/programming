# モジュール

## 準備

1. [Google Colaboratory](https://research.google.com/colaboratory/)で「Python 3の新しいノートブック」を作る．
1. ノートブックの名前を「08」に変える．

## 演習

**問題** 2^3を計算する方法を確認せよ。

```python
import math

math.pow(2, 3)
```

**問題** for文を使って2^3を計算せよ。

**問題** 乱数を発生させる方法を確認せよ。

```python
import random

random.randint(0, 100)
```

**問題** 平均を計算する方法を確認せよ。

```python
import statistics

nums = [1, 5, 33, 12, 46, 33, 2]
statistics.mean(nums)
```

**問題** numsの中央値と最頻値を計算せよ。

**問題** for文を使って平均を計算せよ。

**問題（レポート課題）** for文を使って標準偏差を計算せよ。

**問題（レポート課題）** モジュールを作る方法を確認せよ。（Google Colaboratoryでファイルを作る安直な方法）

```python
!echo "def print_hello():" > hello.py
!echo "    print('Hello')" >> hello.py
```

ファイルができたことを確認する。

```python
!cat hello.py
```

モジュールを読み込み，関数を実行する。

```python
import hello

hello.print_hello()
```

**問題（レポート課題）** モジュール中の動作確認用コードが，import時には実行されないようにする方法を確認せよ。

```python
!echo "print('Hello!')" > module1.py

import module1
```

```python
!echo "if __name__ == '__main__':" > module1.py
!echo "  print('Hello!')" >> module1.py

import module1
```