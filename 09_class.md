# 新しいデータ型を作る

**問題** 6面体のさいころ`Dice`を作る。

```python
class Dice:
  face_num = 6
  def shoot(self):
    return random.randint(1, self.face_num)

```

`face_num`がアトリビュート，`shoot`がメソッドである。（メソッドの最初の引数は`self`とすることになっている。）

このさいころの実体（インスタンス）を作り，さいころを振ってみよ。

**問題** n面体のさいころにする。

```python
class Dice:
  def __init__(self, val):
    self.face_num = val
  def shoot(self):
    return random.randint(1, self.face_num)

```

`__init__`は，インスタンスを作るのに使われる特殊なメソッドで，「初期化メソッド」と呼ばれる。（細かい注意：前問では初期化メソッドを作っていなかったが，そういう場合には初期化メソッドが自動的に作られる。）

12面体のさいころのインスタンスを作り，さいころを振ってみよ。

**問題** 面の数を指定せずにインスタンスを作ると6面体のサイコロになるようにせよ。

**問題（オプショナル）** `Dice`のインスタンス生成時に，「Hello!!」と表示するようにせよ。

**問題（オプショナル）** `Dice`のクラス図を描け。

**問題（オプショナル）** `Dice`の定義をdice.pyに保存しておくと，`import dice`とすれば`myDice = dice.Dice()`などが可能になることを確認せよ。

**問題（オプショナル）** 次のように振る舞うクラス`Person`を実装せよ。

```python
taro = Person("Taro", 12)
taro.eat() #「Taro ate.」と表示される
taro.show()#「Taro (12)」よ表示される

jiro = Person("Jiro", 10)
jiro.eat() #「Jiro ate.」と表示される
jiro.show()#「Jiro (12)」よ表示される

taro.eat() #「Taro ate.」と表示される
taro.show()#「Taro (12)」よ表示される
```

**問題（オプショナル）** Personを継承し，次のように振る舞うクラス`Student`を実装せよ。

```python
taro = Student("Taro", 12, "001")
taro.eat() #「Taro ate.」と表示される
taro.show()#「Taro (12)」よ表示される
taro.study()

jiro = Student("Jiro", 10, "002")
jiro.eat() #「Jiro ate.」と表示される
jiro.show()#「Jiro (12)」よ表示される
jiro.study()
```
