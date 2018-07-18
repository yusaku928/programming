# 関数を作る

**問題** 関数の定義法，呼び出し法を確認せよ。

```python
def func():
  i = 3
  return i

print(func())
```

**問題** 引数を持つ関数の定義法，呼び出し法を確認せよ。

```python
def func(v):
  i = v + 3
  return i

print(func(5))
```

**問題（オプショナル）** 上の問題の関数定義を`c:/cit/my_module.py`というファイル名で保存せよ。コマンドプロンプトで次のコマンドを実行し，作業ディレクトリを移動してからPythonインタラクティブシェルを起動し，そこで次のコードが動くことを確認せよ。

```python
import my_module
my_module.func(5)
```

**問題（オプショナル）** `c:/cit/my_module.py`を次のように変更せよ。

```python
def func(v):
  i = v * 3
  return i
```

Pythonインタラクティブシェルで次のコードを実行すると，関数`func()`の変更が反映されることを確認せよ。

```python
import importlib
importlib.reload(my_module)
```

**問題** 整数nに対して1からnまでの和を返すような関数`total(n)`を作れ。

**問題** 次のプログラムの実行結果を確認せよ。

```python
import turtle
turtle = turtle.Turtle()

def center_circle():
  turtle.penup()
  turtle.forward(200)
  turtle.left(90)
  turtle.pendown()
  turtle.circle(200)
  turtle.left(90)
  turtle.penup()
  turtle.forward(200)
  turtle.pendown()

center_circle()
```

**問題（オプショナル）** 上の関数は次のように書いた方がよい。それはなぜか。

```python
import turtle
turtle = turtle.Turtle()

def center_circle(target):
  target.penup()
  target.forward(200)
  target.left(90)
  target.pendown()
  target.circle(200)
  target.left(90)
  target.penup()
  target.forward(200)
  target.pendown()

center_circle(turtle)
```

**問題** x, y, rを引数とし，中心(x, y)，半径rの円を描く関数`circle(x, y, z)`を書け。

**問題** 上で定義した関数`circle(x, y, z)`を使って，次の絵を描け。（サイズは適当でよいが，この図形はx軸対称かつy軸である。）

![](https://raw.githubusercontent.com/taroyabuki/programming/master/fig/turtle3.png)

**問題** `circle(x, y, z)`を修正し，`circle(10, 20)`のように`r`を省略して呼び出したときは，半径150の円が描かれるようにせよ。

**問題（オプショナル）** `map(関数, リスト)`で，リストの各要素に関数を適用した結果を得る（関数も関数の引数になる）。次のコードでこのことを確認せよ。結果を`list`で囲むとリストになる。

```python
def f(x):
  return x * 2

list(map(f, [1, 2, 3, 4, 5]))
```
