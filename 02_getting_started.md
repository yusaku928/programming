# さあ，はじめよう！

## 準備

教科書：「Pythonのインストール」はやらなくていい．

1. [Google Colaboratory](https://research.google.com/colaboratory/)で「Python 3の新しいノートブック」を作る．
1. ノートブックの名前を「02」に変える．

## 用語

* プログラミング
* コード
* 低水準言語と高水準言語
* アセンブリ言語
* Python

## 演習

参考：アセンブラのコード例（https://github.com/calthoff/self_taught/blob/master/bash_ex0.sh ）をLinuxで実行する方法．

```bash
wget -O hello.asm https://raw.githubusercontent.com/calthoff/self_taught/master/bash_ex0.sh
nasm -f elf64 hello.asm
ld -s hello.o
./a.out
```

作業：Google Colaboratoryに以下のコードを入力し，Shift+Enterで実行する．

```python
print("Hello, World!")
```

**問題：** 別の文字列を表示させる．

**問題：** `print`のスペルを間違えたときのエラーメッセージを日本語に翻訳する．
