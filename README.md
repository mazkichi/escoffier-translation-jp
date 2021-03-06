# エスコフィエ『料理の手引き』全注解　作業用リポジトリ #

-----
## [Github 超初心者むけにパソコンのWEBブラウザで作業に参加する方法](Docs/commit-via-web-browser.md)をまとめました

「協力はしたいけれどどうすればいいかわからない」という方はぜひこのリンク先の[**WEBブラウザでファイルの下準備、下訳、編集、校正に参加する方法**](Docs/commit-via-web-browser.md)をご覧ください。

**このREADMEファイルは「温泉旅館」的に書き足しているので、まったくの初心者の方はまず上のリンク先のファイルからお読みください**。

----
## [急募! 原稿下準備ボランティア](https://github.com/lespoucesverts/escoffier-translation-jp/blob/master/PETITES-ANNONCES.md)

[リンク先 PETITES-ANNONCES.md をご覧ください](https://github.com/lespoucesverts/escoffier-translation-jp/blob/master/PETITES-ANNONCES.md)

-----
## 重要!　文書構造の見直しをおこないました。このため、節やレシピ名の見出しの部分で用いている記号が変わっています(最下部参照)

* XV GLACES ディレクトリ15-glacesのファイルを細かく分割することにしました。

* 原稿ファイル *.mdの冒頭にMarkdownのコメント形式で作業チェックリストを入れました。

* Github のプレビュー画面では原稿ファイルを正しく表示できません。ご注意ください。

-----

## 「チラ見」ファイルの閲覧、ダウンロード ##

* 「チラ見」用のPDFは<>code の最上位ディレクトリにあります。ファイル名は escofier-le-guide-culinaire.pdf です。拡張子にご注意ください。最後が .tex となっているファイルはPDF組版用のものでTeXという組版言語を用いて書かれています。もしお読みになって目まい、頭痛になったとしても自己責任となりますのでご注意を。PDFファイルはブラウザ上でも直接開けるみたいですが、動作がとても遅い可能性があります。

本文は1段組み、レシピは二段組です。PDFの設定上は現在、A4版、文字サイズは14級（近似値的）。パソコンや高解像度のタブレットだと読みやすいでしょう。スマートフォンの場合は、画面の小さな機種では非常に読みづらいかも知れません。


## 編集協力の方法 ##

編集協力者は常時募集中です。Githubのシステム上、アカウントをお持ちであればどなたでも編集にご協力いただけます。

### WEBブラウザで編集する ###

これがいちばん簡単な方法です。Githubでググるとリポジトリをフォークして云々……と出てきますが、**そんなこと気にせずに、このリポジトリのディレクトリにある\*.mdファイルを開いて編集しちゃってみてください**。

### 自分のパソコンで編集する ###

とはいえ、フォークしちゃった、という場合には、お手元のパソコンで好きなエディタを使って作業ができるようにしたいかも知れませんので、「一応」その方法を書いておきます。(あくまでも「参考」程度にしてください。多分、エディタがAtomだともっと簡単に出来る方法もあるように思います)。

1. まず、自分のパソコンの適当なディレクトリ(たとえばMacなら「書類」のなかにEscoffierとでも)フォルダを作ります。

2. Mac の場合は「ターミナル」(アプリケーション>ユーティリティにあります)を開いて、

    cd ~/Documents/Escoffier

と打ち込んでください。Escoffierは先程例に出した新たにつくったフォルダ名です

3. つぎに、ターミナルで自分がフォークしたリポジトリをクローンします。HTTPSを使うのがいまはデフォルトになっているようです。ブラウザで、自分のアカウント/escoffier-translation-jp というフォークしたリポジトリにアクセスして、右の緑のボタンClone or Download をクリックします。さらに、https://github.com から始まる文字列の右側のよくわからんアイコンをクリックしてください。クリップボードにこのフォークされたリポジトリのアドレスがコピーされます。

4. この状態でターミナルに戻ります。

    git clone

と打って、ペースト(コマンド+V)します。

    git clone https://github.com:youraccountongithub/escoffier-translation-jp.git

となったらリターンキーです。

場合によってはしばらく待たされます。

5. これで「あなたがフォークしたエスコフィエのリポジトリがあなたのパソコンにある」状態になります。

6. これだけだと、「**あなたがフォークした時点での**エスコフィエのリポジトリ」の内容に過ぎません。なので、本家と同期させてやります。ターミナルで

    git remote add upstream https://github.com/lespoucesverts/escoffier-translation-jp.git

と打ってください。これで本家に対してupstreamという名前をつけて「つながった」ことになります。

7. 次回から、作業の前や途中でターミナルに

    git fetch upstream
    git checkout master
    git merge upstream/master

と「おまじない」3つ入力をすると、本家とリアムタイムで同一の内容がお手元のパソコンにあるリポジトリにコピーされます。ただし、**本家は一日に何度もアップデートしている**ので、やっぱりこの方法はあんまりお勧めできないかも。この先の段階として、本家に対して自信をもってプルリクエストできる方以外は、ブラウザで直接このリポジトリをいじってプルリクエストする方法をとりあえず採用したほうがいいでしょう。


このあたり、GithubアプリとかAtomとかSourceTreeだともっと直感的に出来るはずなんですが……すみません、やったことがないので、あとはググってください。

ただ、よっぽどバリバリ校正とか下訳を書いてくださるのでなければ、基本的にここまでやる必要はないんです。上で書いたように、ブラウザから直接このリポジトリにあるファイルを編集したほうが圧倒的に簡単だと思います。また、「プルリクエストしたはずなんだけど返事がない……」というようなケースも避けられるでしょう(だいたいが、自分のフォークしたリポジトリに対してだけプルリクエストしているというケースみたいですので)。


### 作業すべきファイル ###


Markdownファイル（.md）が作業ファイル=原稿です。TeXの独自命令が増えてしまったので、markdown と TeX の**ちゃんぽん**のような書式になっています。バックスラッシュ\で始まる文字列がTeXの命令ですが、なんとなく意味はおわかりいただけるように書いているつもりです。

[Pandoc Extended Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)いう書式を用いており（[日本語版はこのリンクの上から1/3くらいのところ](http://sky-y.github.io/site-pandoc-jp/users-guide/)、ただし内容が古いので出来るだけ英語版を参照してください）、このサービスで標準とされている Github Flavored Markdown に準拠していない部分があるため、ブラウザ上でのプレビューは正しく表示されないことがほとんどです。

原稿そのものを適切にプレビューするには、Pandoc Extended Markdown に対応したエディタが必要です。（Atomというエディタの追加パッケージで対応する、markdown preview plus というものがあり、とても便利です）。

**編集協力者は、番号（=章番号）で始まるディレクトリ内のMarkdownファイルに対してのみ編集してコミットするようにしてください**。（以下にファイル名を列挙しておきます）

命名規則は

章番号-節番号-pp原書のページ範囲.md

* 00-avant-propos/00-avant-propos.md
* 01-sauces/01-01-pp1-12.md
* 01-sauces/01-02-pp13-17.md
* 01-sauces/01-03-pp18-27.md
* 01-sauces/01-04-pp28-41.md
* 01-sauces/01-05-pp42-46.md
* 01-sauces/01-06-pp47-52.md
* 01-sauces/01-07-pp53-57.md
* 01-sauces/01-08-pp58-62.md
* 01-sauces/01-09-pp63-67.md
* 02-garnitures/02-01-pp68-77.md
* 02-garnitures/02-02-pp78-82.md
* 02-garnitures/02-03-pp83-88.md


**慣れないうちは、これらのファイルに対してだけ変更をコミットしてください。**

もちろん、これらのファイルを参考にして、まだ訳と注釈をつけていない部分のファイルを作成してプッシュしたくださることは大歓迎です。

PDFは適時マージされます。単に組版イメージ確認のためであり、「チラ見」用です。

それ以外のファイル（TeX関連が主です）は、Lualatex を分る方以外は触らないようにご注意ください。目まいがするか、頭が痛くなっても責任は負えません。

原稿ファイル（.md）には時折\{\#fonds-blanc-volaille\} のようなものが見出しにありますが、これはPDFやHTML、EPUBで内部リンクを張るための「ラベル」です。原書の項目名を、すべて小文字」にしてアクサンなし、ハイフンでつないでいます。


### Markdownファイル=原稿はブラウザ上で作業可能です ###

**上で述べたように、これがいちばん簡単な方法です**。ブラウザでこのリポジトリを開き、ソース>目的の章のディレクトリ>作業ファイル、と進んでください。

.md ファイルをクリックして開くとMarkdownのプレビューモードで表示されます。右上にある「編集」=鉛筆のマークをクリックして編集モードに移行します。間違ってもその隣の「ゴミ箱」をクリックしないでください。

この状態で**誤字、脱字、明らかなミスについては直接書き込んでください**。その後、

1. 上のほうにある Preview Changes を押して変更内容を確認します。環境によってはちょっと待たされることがあります。
2. OKであれば、スクロールして下の方にある Create a new branch for this commit and start a pull request. の左のラジオボタンが選択されていることを確認し、上のコメント覧に変更内容等を書いてください。
3. 大きなボタン Commit Changes を押します。
4. 画面が変わり、Create a Pull Request なんたらという表示が出るので、再確認ボタンを押すと「プルリクエスト」が作成されたことになります。この時点ではこのリポジトリのファイルに変更は加えられていません。要するに「変更の提案」ということです。このときにコメント欄があります。これが主な議論の場となりますので活用してください。
5. プルリクエストがあると、僕が変更内容を確認し、妥当と判断すればマージ（ファイルに取り込むこと）します。

#### ローカルルール #####

* 数字は一桁のものも半角数字を用いてください（全角は用いないでください）。前後にスペースを入れる必要はありません（とりわけ禁則文字、役物の一部が自動処理されずに問題が発生することが確認されました）。
* ただし、単位を表す mL, dL, L, g, kg, mm, cm なども半角文字を使いますが、これら単位の直前、つまり半角数字の直後には半角スペースを挟んでください。（例） ワイン1 dL、

これらはTeXで処理する際に、自動的に適当に文字間を調整して表示されます。


#### 注釈の編集、追加方法 ####

すでにある注釈に変更を加える場合は、直接書き込んでください。その直後に\[\](○○変更)のようにコメントがあるとわかりやすいでしょう。

あらたに注釈を追加する場合、すでにある番号とダブってしまうとエラーの原因になりますので、

    本文[^15]本文本文[^15bis]本文本文本文
    本文本文本文。

    [^15]: すでにある注釈だけどここは変更[](20180129○○変更)注釈文の続き

    [^15bis]: あらたに追加した注釈

のように、直前の注釈番号にbisをつけてください。すでに直前のものにbisがついている場合は、bis2、bis3のようにして、かならず番号がダブらないようご注意ください。また、注釈は対象の段落の直後がわかりやすくて便利です。

#### TeX命令文が含まれています ###

基本的に、TeXという組版プログラム群を使う前提の md ファイルです。そのため、markdown の書式ではないTeX命令の行がしばしばあり、プレビュー状態でも表示されてしまいます。

    \index{garniture@garniture!madeleine@--- Madeleine}
    \index{madeleine@Madeleine!garniture@garuniture ---}
    \index{かるにちゆーる@ガルニチュール!まとれーぬ@---・マドレーヌ}
    \index{まとれーぬ@マドレーヌ!かるにちゆーる@ガルニチュール・---}


あるいは

    \newpage

あるいは

    文章\ruby{漢字}{ふりがな}

など。



#### 分数の表示はMarkdownで一般によく使われているTeX表記です #####

##### 表記

    $\frac{分子}{分母}$

つまり

    1/2 = $\frac{1}{2}$

という感じになります。分子と分母がわかれば数字のチェックも可能だと思います。

**TeXに不慣れな方はバックスラッシュ\で始まるこれらの表現には触れないようにしてください**。お願いします。

#### 編集コメント ####

短かいコメントは**文中に**、少し長いなら、該当段落の下にカラ行を多めに入れてあるので、そこに、

    [](コメント)

として書いてください。\[と\]の間はスペースなし。**半角記号**です。カッコも必ず**半角**にしてください。多少長くなっても大丈夫ですが、余分な改行は入れないほうがコメント行としてきちんと機能する可能性が高いので、改行しないようお願いします。

編集モードでこの行の下を見るとコメントの実例が見られます。

[](これはコメントの例です)

このようにして書いたコメントは「プレビュー」モードで表示されなくなりますが、編集モードとdiff表示において表示されます。

長いコメントは、コミットする際（後述）にコメント欄がありますので、そこでも大丈夫です。


### コミット ###

とても**大事なこと**なので2度書きます。

ブラウザ上で編集した場合、作業後に

1. 上のほうにある Preview Changes を押して変更内容を確認します。環境によってはちょっと待たされることがあります。
2. OKであれば、スクロールして下の方にある Create a new branch for this commit and start a pull request. の左のラジオボタンが選択されていることを確認し、上のコメント覧に変更内容等を書いてください。
3. 大きなボタン Commit Changes を押します。
4. 画面が変わり、Create a Pull Request なんたらという表示が出るので、再確認ボタンを押すと「プルリクエスト」が作成されたことになります。この時点ではこのリポジトリのファイルに変更は加えられていません。要するに「変更の提案」ということです。このときにコメント欄があります。これが主な議論の場となりますので活用してください。
5. プルリクエストがあると、僕が変更内容を確認し、妥当と判断すればマージ（ファイルに取り込むこと）します。

**プルリクエストがマージされた後に、pandocでいったんTeXファイルに変換、必要な処置をしてからPDF化するので、マージ直後にPDFに修正が反映されるわけではありません**。

### Markdownプレビューモードでの注番号について ###

**Githubでのプレビューモードでは、注が正しく表示されません**。ダウンロードしてMarkdown対応エディタのプレビューを使うか、pandocで適宜変換してください。


### ブラウザ上で編集する際の注意 ###

ブラウザ上で編集する場合、「コミット」が完了するまで変更した内容が保存されません。僕はよくやってしまうのですが、誤ってページのリロード、バックなどしてしまうと、それまでの編集内容が全て失なわれてしまいます。

そのため、多少煩雑になっても、1ファイルまとめて全部徹底的に、ではなく、数回に分けて編集、コミットするほうが安全です。

あるいは、エディタにコピペして作業し、それを戻していただいても結構ですが、その場合は、**余計な空白行などが入らない**ようご注意ください。Diffによる変更点の比較がうまくいかなくなりますので。

もっとも、エディタで作業できるのであれば、Githubアプリをお使いいただくほうが便利だと思います。

### 見出しの階層 ###

* \# 章(ソース、ガルニチュール etc）= chapter
* \#\# 節（基本ソース、茶色い派生ソース etc.）= section
* \frasec{section en fr} 節のフランス語表記。注をここにはつけない。上の\#\# の節につける。
* \#\#\# 小節 = subsection
* \frasecb{subsection-b en fr} 小節のフランス語表記(節よりやや小さい文字サイズを使用)。注も上の日本語部分につけること。
* \#\#\#\# レシピ名
* \frasub{recette en fr} レシピ名のフランス語表記。これも注は不可。
* \#\#\#\#\# 予備
* \#\#\#\#\#\# 原注ほか

※ フランス語見出し\frasub{Nom de recette} にどうしても注をつける場合はLaTeXの注の方式なら大丈夫です。\frasub{Nom\protect\footnote{Voici une note} de recette} のようになります。原稿の可読性が大きく下がるので、出来るだけ日本語部分にMarkdown書式で注をつけるようにしましょう。

<br /><br /><br />
©Manabu GOTO 2018 All Rigths Reserved
