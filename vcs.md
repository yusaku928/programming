# バージョン管理・Anacondaのインストール

## バージョン管理

### 準備

1. https://github.com/ でアカウントを作る（sign up）。ヒント：「github アカウント 作成」で検索。
1. Verify email address.
1. https://desktop.github.com/ でGitHub Desktopをダウンロードし，インストールする。
1. GitHub Desktopを起動し，GitHubのアカウント情報を追加する。

### 自分のリポジトリ

1. GitHubにログインする。（sign in）
1. リポジトリを作る。リポジトリ名は好きに決めてよい。
1. GitHub Desktopで，作ったリポジトリをローカル（自分のパソコン）cloneする。
1. ローカルで適当なファイルを作成する。
1. コミット！
1. プッシュ！
1. （別の人のつもりで）ウェブ上でファイルを作る。
1. ローカルでプル！

**問題（オプショナル）** ウェブ上でファイルを変更した後，ローカルでプルする前にコミット・プッシュしようとするとどうなるか。そこで起きた問題はどうやって解決すればいいだろうか。

### 他人のリポジトリ

1. https://github.com/taroyabuki/programming をForkする。
1. GitHub Desktopで，Forkしたリポジトリをローカル（自分のパソコン）cloneする。
1. フォルダstudentsの中に，自分の学生番号（例：`1234567`）をファイル名とするテキストファイルを作る。
1. コミット！
1. プッシュ！
1. GitHub上でpull requestを作成する。
1. （矢吹がpull requestを受け入れた後）https://github.com/taroyabuki/programming/tree/master/students の中に自分の学生番号のファイルがあることを確認する。（期末試験に10点加算する。ただし，加算後の点数は最高でも40とする。）

## Anaconda

1. [Anaconda](https://www.anaconda.com/download/)をインストールする。
1. Anaconda PromptからPythonを起動し，`exit()`または`quit()`で終了する。

### 作業ディレクトリ

Anaconda Promptで以下を実行する。

```bash
c:
cd /
mkdir cit
cd cit
```

### Jupyter notebook

Anaconda Promptで以下を実行する。

```bash
c:
cd /cit
jupyter notebook
```

**問題** Jupyter notebook上でPythonの新しいファイルを作る。そのファイルがc:/citにあることを，コマンドプロンプトとエクスプローラで確認せよ。