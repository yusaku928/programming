# バージョン管理・Anacondaのインストール

## Anacondaのインストール

[Anaconda](https://www.anaconda.com/download/)をダウンロードする（Python 3系）。ダウンロードには時間がかかるから，それを待つ間に次の「バージョン管理」を進めておく。

ダウンロードが終わったらインストールする。インストールはすべてデフォルトのまま進めてよいが，途中でVisual Studio Codeのインストールについて聞かれたら，「Install Microsoft VSCode」をクリックしてインストールする。それをSkipしてしまった場合は，https://code.visualstudio.com/ に行ってダウンロード，インストールすればよい。

Windowsのユーザ名に非ASCII文字が含まれていると，デフォルトのままではインストールできない。以下のような解決策がある。

* （推奨）Windowsのユーザを新たに作る。ユーザ名はASCII文字だけにする。**ユーザ名の変更は推奨しない（他に影響があるかもしれない）。**
* インストール先を変更する（例：`c:/cit/Anaconda3`）
* Install for:を「Just Me」ではなく「All Users」にする。
* [Chocolatey](https://chocolatey.org/)でインストールする。（`cinst -y Anaconda3'）

## バージョン管理

### 準備

1. https://github.com/ でアカウントを作る（sign up）。ヒント：「github アカウント 作成」で検索。
1. Verify email address.
1. https://desktop.github.com/ でGitHub Desktopをダウンロードし，インストールする。
1. GitHub Desktopを起動し，GitHubのアカウント情報を追加する。

Windowsのユーザ名に全角スペースが含まれていると，GiHub Desktop 1.2.3は正しく動作しない（プッシュができない）。以下のような解決策がある。

* （推奨）Windowsのユーザを新たに作る。ユーザ名はASCII文字だけにする。ユーザ名に非ASCII文字を使っていると，将来他のことでも問題が起こる危険性があるから，早く変えてしまった方がいい。**ユーザ名の変更は推奨しない（他に影響があるかもしれない）。**
* 別のGitクライアントを使う。（例：SourceTreeは強力。日本語化もされている。ただし，利用時にユーザ登録が必要。）
* コマンドプロンプトでプッシュする。そのために，https://git-scm.com/downloads からGitをダウンロード，インストールし，GitHub Desktopを再起動する。GUIでプッシュする代わりに，Repositoryメニューの「Open in Command Prompt」をクリックし，`git push origin`を実行する。

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

## Anacondaの実行

Anaconda Promptから`python`でPythonを起動し，`exit()`または`quit()`で終了する。

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
