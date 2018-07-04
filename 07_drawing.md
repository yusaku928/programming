# Pythonで画を描く

[モジュールturtleのリファレンスマニュアル](https://docs.python.jp/3.6/library/turtle.html)を参考に，以下の問題に解答せよ。（これはマニュアルを読む練習でもある。）

Anaconda Promptで`python`としてインタラクティブシェルを起動して先に進む。

**問題** 次のようにして、モジュールturtleが起動することを確かめよ。（教科書では`kame`という名前を使っているが，ここではリファレンスマニュアルに合わせて`turtle`としている。）

```python
import turtle
turtle = turtle.Turtle()
turtle.position()
#end
```

動作が不安定になったら、一度`quit()`で終了しインタラクティブシェルを再起動するといい。

**問題** 次のコードで描かれる図形は何か。

```python
turtle.home()
turtle.clear()
turtle.forward(200)
turtle.left(120)
turtle.forward(200)
turtle.left(120)
turtle.forward(200)
#end
```

**問題** 次のコードで描かれる図形は何か。（`for`文を終わらせるために、最後に空行が必要。）

```python
turtle.home()
turtle.clear()

for i in range(3):
  turtle.forward(200)
  turtle.left(120)

#end
```

**問題** 次のコードで描かれる図形は何か。

```python
turtle.home()
turtle.clear()

for i in range(5):
  turtle.forward(200)
  turtle.left(144)

#end
```

**問題** 次の絵を描け。（サイズは適当でよい。）　ヒント：繰り返しやすい部分を考えよ。

![](https://raw.githubusercontent.com/taroyabuki/programming/master/fig/turtle1.png)

**問題** 次の絵を描け。（サイズは適当でよい。）

![](https://raw.githubusercontent.com/taroyabuki/programming/master/fig/turtle2.png)

**問題** 次は何をするコードか。（`Ctrl+C`で停止）

```python
import random

turtle.home()
turtle.clear()

while True:
  turtle.left(random.randint(1, 360))
  turtle.forward(15)

#end
```

**問題** 次は何をするコードか。（`Ctrl+C`で停止）

```python
import random

r = 100
turtle.home()
turtle.clear()

while turtle.distance(0, 0) < r:
  turtle.left(random.randint(1,360))
  turtle.forward(15)

#end
```

**問題（オプショナル）** 次は何をするコードか。（`Ctrl+C`で停止）

```python
import random

r = 100
turtle.home()
turtle.clear()
turtle.penup()
turtle.forward(r)
turtle.left(90)
turtle.pendown()
turtle.circle(r)
turtle.penup()
turtle.home()
turtle.pendown()

while turtle.distance(0, 0) < r:
  turtle.left(random.randint(1, 360))
  turtle.forward(15)

#end
```
