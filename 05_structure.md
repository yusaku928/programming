# 条件分岐と繰り返し

## for文

**問題** 次のプログラムの実行結果を確認せよ。

```python
myList = [5349, 5478, 5344, 4644, 4968, 6259]

for val in myList:
  print(val)

```

**問題** 次のプログラムの動作を説明せよ。

```python
myAvg = 0.
for val in myList:
  myAvg += val

myAvg /= len(myList)
print(myAvg)
```

**問題** ```myList2 = [3148, 2991, 2966, 2457]```の平均を求めよ。（ヒント：この段階では，ほぼ同じコードを2回書いてかまわない。）

**問題** Pythonには平均を求める関数```mean()```が用意されている。以下のコードの一部を補い，この関数の動作を試せ。

```python
from statistics import *

print(mean(           ))
```

**問題** （オプショナル）繰り返し構文（つまり`for`）を使って，`myList`と`myList2`の標準偏差を求めよ。その結果を，関数`pstdev()`で計算した結果と比較せよ。

**問題** 次のプログラムの実行結果を確認せよ。

```python
myDic = {'aomori': 5349, 'akita': 4644, 'sendai': 5344, 'Yamagata': 4968, 'fukushima': 6259, 'morioka': 5478}

for key in myDic:
  print(key)

```

**問題** 次のプログラムの実行結果を確認せよ。

```python
for key in myDic:
  print(myDic[key])

```

**問題** 上のコードを使って，```myDic```の値の平均を求めよ。

**問題** 次のコードをヒントにして，```myDic```の値の平均を求めよ。

```python
print(myDic.values())
```

**問題（オプショナル）** myDicのキーを，アルファベット順に表示せよ。


## if文

**問題** ```a```の値を変えて，「大きい」と表示されるようにせよ。

```python
a = 4
b = 4

if a > b:
  print('大きい')

```

**問題** ```b```の値を変えて，「大きくない」と表示されるようにせよ。

```python
a = 5
b = 4

if a > b:
  print('大きい')

if a <= b:
  print('大きくない')

```

**問題** ```a```の値が```b```の値より大きいときは「大きい」，```a```の値が```b```の値より小さいときは「小さい」，```a```の値と```b```の値が等しいときは「等しい」と表示するプログラムを書け。（ヒント：```elif```と```else```を使え。）


## while文

**問題** 下は何をするコードか。

```python
import random
random.randint(1, 6)
```

**問題** 下は何をするコードか。

```python
import random

rand_num = 1

while rand_num != 4:
  rand_num = random.randint(1, 6)
  print(rand_num)

```

**問題** 下は何をするコードか。

```python
import random

while True:
  rand_num = random.randint(1, 6)
  print(rand_num)
  if rand_num == 4:
    break
  print('.')

```

**問題** 下は何をするコードか。上のコードとの違いを含めて説明せよ。

```python
import random

while True:
  rand_num = random.randint(1, 6)
  print(rand_num)
  if rand_num == 4:
    continue
  print('.')

```

**問題** 次のプログラムを実行するとどうなるか。

```python
for x in range(1, 11):
  print(x)

```

**問題** 1から20までの整数を表示するプログラムをfor文を使って書け。

**問題（オプショナル）** 1から20までの整数を表示するプログラムをwhile文を使って書け。

**問題** 1から20までの整数を表示するプログラムを書け。ただし，数が3の倍数の時は数の代わりにFizzと表示せよ。

**問題** 1から20までの整数を表示するプログラムを書け。ただし，数が5の倍数の時は数の代わりにBuzzと表示せよ。

**問題** 1から20までの整数を表示するプログラムを書け。ただし，数が3と5の倍数の時は数の代わりにFuzz Buzzと表示せよ。

**問題（オプショナル）** 1から20までの整数を表示するプログラムを書け。ただし，数が3の倍数の時は数の代わりにFizzと，数が5の倍数の時は数の代わりにBuzzと，3と5の倍数の時は数の代わりにFizz Buzzと表示せよ。（たとえば数が15のときはFizz Buzzと表示する。）

**問題（オプショナル）** 上のプログラムの説明にはあいまいな部分がある。その部分を修正せよ。

## 教科書についてのコメント

* p.115 代わりになる道がないというが，繰り返しは「再帰」で代替可能。
* p.120 最初の補足：削除すべき。
* p.141 「Shift-JIS」は「Shift_JIS」の間違い。
* p.141 OSに依存しない書き方がないと，モジュールを作れなくなってしまう。
