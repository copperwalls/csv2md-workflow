CSV to Markdown
===============

Wouldn’t it be nice if you can edit [Markdown] \([Extra]\) [tables] in [Numbers] or [Microsoft Excel] or [LibreOffice]? Yes?

It’s quite simple, actually. At work we’re using [DokuWiki] with the [MarkdownExtra Plugin]. Here are the steps:

1. Highlight then copy the table from wiki
2. Paste it inside the Numbers app
3. Edit to your heart’s content
4. After editing, File → Export To → CSV...
5. Convert the CSV to Markdown
6. Copy the resulting Markdown
7. Paste and save it on DokuWiki

This [Automator] workflow is for automating 5 and 6 above.

## How to Install ##

1. Clone this repo (or [download the archive directly])

        $ git clone https://github.com/copperwalls/csv2md-workflow.git

2. Open the directory (or unzip the file manually)

        $ open csv2md-workflow

Then just double-click the workflow and _Install_ it as a “Service”.

![alt text][Service Installer screenshot]

## How to Use ##

1. Right-click on the (exported) CSV file
2. Choose “CSV to Markdown” on the Services menu
3. Paste the result somewhere

## How Does It Work ##

Inside the workflow is just a quick hack using [a bunch of Terminal commands]. In fact, since those commands should be available by default on Linux or other BSDs, they can be used on those systems as well.

On OS X, after the CSV is converted to Markdown, the results are [copied automatically]. The resulting Markdown file is also opened automatically using a [couple of applications] if available, [MacVim] and [Marked 2]. Feel free to [change it].

## License ##

Copyright (c) 2016 ed.o

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[Markdown]: http://daringfireball.net/projects/markdown
[Extra]: https://michelf.ca/projects/php-markdown/extra/
[tables]: https://michelf.ca/projects/php-markdown/extra/#table
[Numbers]: https://www.apple.com/mac/numbers/
[Microsoft Excel]: http://office.microsoft.com/en-us/excel
[LibreOffice]: https://www.libreoffice.org/
[DokuWiki]: https://www.dokuwiki.org/
[MarkdownExtra Plugin]: https://www.dokuwiki.org/plugin:markdownextra
[Automator]: https://en.wikipedia.org/wiki/List_of_OS_X_components#Automator
[download the archive directly]: https://github.com/copperwalls/csv2md-workflow/archive/master.zip
[Service Installer screenshot]: https://github.com/copperwalls/csv2md-workflow/blob/master/screenshots/Service_Installer.png "Service Installer—Click Install"
[a bunch of Terminal commands]: https://github.com/copperwalls/csv2md-workflow/blob/master/CSV%20to%20Markdown.workflow/Contents/document.wflow#L82
[copied automatically]: https://github.com/copperwalls/csv2md-workflow/blob/master/CSV%20to%20Markdown.workflow/Contents/document.wflow#L89
[couple of applications]: https://github.com/copperwalls/csv2md-workflow/blob/master/CSV%20to%20Markdown.workflow/Contents/document.wflow#L92
[MacVim]: http://macvim-dev.github.io/macvim/
[Marked 2]: http://marked2app.com
[change it]: https://www.raywenderlich.com/58986/automator-for-mac-tutorial-and-examples

