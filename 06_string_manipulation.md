# 文字列操作

## 準備

1. [Google Colaboratory](https://research.google.com/colaboratory/)で「Python 3の新しいノートブック」を作る．
1. ノートブックの名前を「06」に変える．

## 演習

**問題** 改行を含む文字列の動作を調べよ．

```python
a = '''た
て
よ
み
'''

print(a)

a
```

**問題** 文字列から文字を取得する方法を確認せよ．

```python
name = 'Yabuki'

print(name[0])
print(name[1])
print(name[-1])
print(name[6])
```

**問題** 文字列の足し算と掛け算の結果を確認せよ．

```python
print("Hello" + ", " + "World!")

print("Hello " * 3)
```

**問題** 文字列のメソッド`upper()`，`lower()`，`capitalize()`の動作を調べよ．ヒント：https://docs.python.org/ja/3/library/stdtypes.html?highlight=upper#string-methods

**問題** 文字列を整形する方法を確認せよ．

```python
name = "夏目漱石"
year = 1867

print('{0}は{1}年に生まれた．'.format(name, year))
print(f'{name}は{year}年に生まれた．') # Python 3.6以降
```

**問題** 文字列を分割する方法を確認せよ．

```python
'This is a pen.'.split(' ')
```

**問題** 文字列を結合する方法を確認せよ．

```python
'-'.join(['A', 'B', 'C'])
```

**問題** 文字列の前後の空白を除去する方法を確認せよ．

```python
str = '   前後に空白   '
print(str)

str2 = str.strip()
print(str2)
```

**問題** 文字列の前後の空白を除去する方法を確認せよ．

```python
str = '   前後に空白   '
print(str)
print(str.strip())
```

**問題** 文字列から文字を検索する方法を確認せよ．

```python
print('animals'.index('m'))
print('animals'.index('z'))
```

**問題** 上の問いの例外に対処せよ．

**問題** 文字列Aに文字列Bが含まれているかどうかを調べる方法を確認せよ．

```python
'pen' in 'This is a pen.'
```

**問題** エラーを修正せよ（文章中の引用符がおかしいことは今は気にしない）．補足：想定していない回答：`"This 'is' a pen."`

```python
'This 'is' a pen.'
```

**問題** スライスの例を試せ．

```python
a = [10, 20, 30, 40]

a[1:2]
a[:2]
a[2:]
```

**問題（レポート課題）** `['This', 'is', 'a', 'pen']`をもとに`'THis is a pen.'`を作れ．「`.`」の前には空白はないことに注意．

