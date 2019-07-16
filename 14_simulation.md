# シミュレーション

## 準備

1. [Google Colaboratory](https://research.google.com/colaboratory/)で「Python 3の新しいノートブック」を作る．
1. ノートブックの名前を「14」に変える．

## 演習

**問題** 理想的なコインを30回投げて表が出る回数をXとする。次の問に答えよ。

* （シミュレーション）実験を10回行い，Xの平均と分散を求めよ。
* （理論）二項分布の期待値と分散をWikipediaで調べ，n=30，p=0.5の時の値を求めよ。

**問題（レポート課題）** 上の問題のシミュレーションを[numpy.random.binomial](https://docs.scipy.org/doc/numpy-1.14.0/reference/generated/numpy.random.binomial.html)で，理論的な計算を[scipy.stats.binom](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.binom.html)で実行せよ。

**問題** （シミュレーション）コインを100回投げて、表か裏が10回連続で出る確率は？　参考：[エレガントな解法、エレファントな解法](https://note.mu/issei_y/n/n882e9f77e8bd)

**問題** （理論）コインを100回投げて、表か裏が10回連続で出る確率を正確に求めよ。