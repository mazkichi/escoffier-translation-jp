# エディタ ATOM の使用法

Github 謹製のエディタ Atom は操作方法もそこそこわかりやすく、とても優秀なエディタです。エディタとは「ワープロ」と違いプログラムのソースコードやWEBサイトのhtml, php そして Markdown ドキュメントを書くのに使う、ひたすら文字を入力するということに特化したアプリです。つまり、文字の装飾とかそういう機能が付いていないものです。

さて、この Atom はエディタとしてはかなり新参者で、**重い**のと**OSによっては**やや不安定**、開発スピードが早くて**追従しきれていないパッケージが頻出する**という欠点はあります。また、Emacs と比べるとスピードと機能面で見劣りしますし、Vimの安定性には遠く及びません。とはいえ、デフォルトのただインストールした状態でもそこそこお洒落な見た目で、これからが期待できるでしょう。


これまでのところ、『料理の手引き』全注解プロジェクトでは「イチオシ」のエディタということにしてあります（ちょっと意見が変わりつつあり、Emacsも推薦していこうかな、と考えています）。

## 1.　DLとインストール

まずはエディタ [ATOMをhttps://atom.io/](https://atom.io/)からDLしてインストールしてください。Windows, Mac, Linux 対応です。Mac の場合は zip ファイルがDLされて、ダブルクリックするとアーカイブユーティリティが「解凍」して Atom.app が出来ます。そのまま起動させてもいいですが、「アプリケーション」フォルダに移動させておきましょう。Linux も Ubuntu のような Debian 系の場合は、ダウンロードしたファイルをダブルクリックするとインストール画面になりますので大丈夫です。Windows のことはわかりませんが、ユーザー数が多いOSなので情報はいくらでも見つかると思います。

![](img/atom-001.png)

## 2.　追加パッケージ

追加パッケージをATOMのメニューのPreference>Installで導入します。Preference メニューはOSによって場所が違うようなのですが、Macの場合はリンゴマークの右、**Atomのメニュー項目のやや上の方** にあります。Linux は **Edit メニュー項目の下のほうです**。

### このプロジェクトで Atom を便利に使うのに「あったほうがいい」パッケージ

1. japanese-menu （日本語化パッケージ）
2. markdown-preview-plus （プレビュー用パッケージ）
3. reflow-japanese (設定で文字長を80にしてください、日本語40文字できれいに自動で強制改行してくれます）
4. markdown-writer (Markdown書式を覚えていない場合）
5. wordcount (ファイルの文字数表示、2バイト文字も1文字としてきちんと表示されます）

### pandoc のインストール

Atom とは別に、分数表記を Markdown Preview Plus で見られるようにするには pandoc というプログラムをインストールする必要があります
http://pandoc.org/
からご使いのOSに対応したものをDLしてインストールしてください。

![](img/atom-002.png)

インストール Installing のところを押すと各OSについてのインストールの説明があります。

![](img/atom-003.png)

Macの場合は、最初に書いてあるように [homebrew](https://brew.sh/)をインストールしてからターミナルで

    brew install pandoc

とするのがいちばん簡単です。時々、

    brew Update

してやり、pandoc のアップデートが報告されていたら

    brew upgrade

で OK です。僕はこの方式をとっているのですが……

が、この方法には**重大な欠点**があって、XCodeなる apple 謹製の開発プログラム一式を入れろだのなんだのという必要があります。いろいろやるのに Homebrew そのものは手軽でいいんですが、こんな使いもしないアップルのプログラム開発アプリを入れろってのはちょっと……**

そういう場合は、download page に行って、**ご自分のOSに合わせた最新版をダウンロードしてインストール**という方法をとってください**。

![](img/atom-004.png)

#### 重要

**pandoc**はコマンドラインツール、つまりMacやLinuxの「ターミナル」にコマンドを打ち込んで使うものです。ただ、Atom で Markdown Preview Plus の機能を使うぶんには **何もしなくていいです。入れっぱなしでとりあえずOKです**。

## 3.　Atom を使ってみる

![](img/atom-005.png)

いまこのドキュメントを書いているスクリーンショットです。左からプロジェクトのフォルダにあるファイル一覧、行番号のついているのが atom.md という名前のこのファイルそのもの、中央より右が Markdown Preview Plus によるプレビューです。そこそこ使える感じしませんか? 右端は Git の操作ペインです。

### Markdown Preview Plus を活用した「誤字、脱字チェック」

#### 自分のパソコンのハードディスクにプロジェクトのリポジトリをクローンする

まずは自分のパソコンにプロジェクトのフォルダを複製します。ターミナル（アプリケーション>ユーティリティにあります）を開いて、プロジェクト専用のフォルダを作ります。たとえば

    mkdir ~/Documents/github

とすると、「書類」フォルダの中に github という名前のフォルダが作られています。またターミナルに戻って、そこにプロンプトを移動させます

    cd ~/Documents/github

次に、プロジェクトのファイル一式をまとめてDLしてしまいます

    git clone https://github.com/lespoucesverts/escoffier-translation-jp.git

[](ここで本文にちょっと変更を加えてみます)