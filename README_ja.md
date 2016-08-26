CSV to Markdown
===============

[Markdown] \([Extra]\)の[テーブル]を[Numbers]か[Microsoft Excel]か[LibreOffice]で編集できたらいいすよね？

実は簡単です。職場では[DokuWiki]に[MarkdownExtraのプラグイン]を使ってます。手順は以下の通りです。

1. Wikiにあるテーブルをハイライト→コピーして
2. Numbersに貼り付けて
3. 好きなだけ編集して
4. ファイル → 書き出す → CSV... ファイルとして保存して
5. そのCSVをMarkdownに変換して
6. 結果をコピーして
7. Dokuwikiに貼り付けて

完了です。

本[Automator]ワークフローは上記の5と6を自動化するためのものです。


## インストール方法 ##

1. 本レポをクローンして（または，[圧縮ファイルを直接ダウンロード]して）

        $ git clone https://github.com/copperwalls/csv2md-workflow.git

2. クローンされたディレクトリーを開いて（圧縮ファイルを直接ダウンロードしたならそれを解凍して）

        $ open csv2md-workflow

あとは，そのディレクトリー内にあるワークフローをダブルクリックして，“サービス”としてインストールすれば良いです。

![alt text][サービスインストーラースクリーンショット]

## 使い方 ##

1. CSVファイルを右クリックして
2. サービスメニュー内にある“CSV to Markdown”を選択して
3. 結果をどこかに貼り付ければ良い

注意: UTF-8でエンコードされたCSVファイルのみに対応しています。LibreOfficeかNumbersで作成したCSVファイルにはそのまま使えます。

## どういう動きをするのか ##

ワークフロー中には簡単に[組み合わせしたターミナルコマンド]が含まれています。実は，Linuxまたは他のBSD系のシステムにそれらのコマンドはデフォルトで含まれているため，それらのシステムでも実行できます。

OS Xでは，CSVからMarkdownへ変換後に，結果は[自動的にコピーされます]。出力されるMarkdownファイルは[2つのアプリ]，[MacVim]と[Marked 2]，で（インストールされていれば）自動的に開かれます。挙動を自由に[変更してください]。


## ライセンス ##

Copyright (c) 2016 ed.o

以下に定める条件に従い，本ソフトウェアおよび関連文書のファイル（以下「ソフトウェア」）の複製を取得するすべての人に対し，ソフトウェアを無制限に扱うことを無償で許可します。これには，ソフトウェアの複製を使用，複写，変更，結合，掲載，頒布，サブライセンス，および/または販売する権利，およびソフトウェアを提供する相手に同じことを許可する権利も無制限に含まれます。

上記の著作権表示および本許諾表示を，ソフトウェアのすべての複製または重要な部分に記載するものとします。

ソフトウェアは「現状のまま」で，明示であるか暗黙であるかを問わず，何らの保証もなく提供されます。ここでいう保証とは，商品性，特定の目的への適合性，および権利非侵害についての保証も含みますが，それに限定されるものではありません。 作者または著作権者は，契約行為，不法行為，またはそれ以外であろうと，ソフトウェアに起因または関連し，あるいはソフトウェアの使用またはその他の扱いによって生じる一切の請求，損害，その他の義務について何らの責任も負わないものとします。


[Markdown]: http://www.markdown.jp/what-is-markdown/
[Extra]: https://michelf.ca/projects/php-markdown/extra/
[テーブル]: https://michelf.ca/projects/php-markdown/extra/#table
[Numbers]: https://www.apple.com/jp/mac/numbers/
[Microsoft Excel]: https://products.office.com/ja-JP/excel
[LibreOffice]: https://ja.wikipedia.org/wiki/LibreOffice
[DokuWiki]: https://www.dokuwiki.org/ja:dokuwiki
[MarkdownExtraのプラグイン]: https://www.dokuwiki.org/plugin:markdownextra
[Automator]: https://duckduckgo.com/?q=OS+X+Automator+とは
[圧縮ファイルを直接ダウンロード]: https://github.com/copperwalls/csv2md-workflow/archive/master.zip
[サービスインストーラースクリーンショット]: https://github.com/copperwalls/csv2md-workflow/blob/master/screenshots/Service_Installer_ja.png "サービスインストーラー クリックしてインストール"
[組み合わせしたターミナルコマンド]: https://github.com/copperwalls/csv2md-workflow/blob/master/CSV%20to%20Markdown.workflow/Contents/document.wflow#L82
[自動的にコピーされます]: https://github.com/copperwalls/csv2md-workflow/blob/master/CSV%20to%20Markdown.workflow/Contents/document.wflow#L89
[2つのアプリ]: https://github.com/copperwalls/csv2md-workflow/blob/master/CSV%20to%20Markdown.workflow/Contents/document.wflow#L92
[MacVim]: http://macvim-dev.github.io/macvim/
[Marked 2]: http://marked2app.com
[変更してください]: https://duckduckgo.com/?q=Automatorの編集方法

