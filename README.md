# Description

A simple script which uses the Wikipedia API (or wiki API of your choice) to turn Wiki markup into HTML.

# Example Usage

```shell
$ cat test.wiki
= Page Title =

Hello, I am some '''bold text''' and some ''italic text''.

$ ./wiki-parse --file test.wiki --output test.html

$ head test.html
<h1><span class="mw-headline" id="Page_Title">Page Title</span><span class="mw-editsection"><span class="mw-editsection-bracket">[</span><a href="/w/index.php?title=API&amp;action=edit&amp;section=1" class="mw-redirect" title="Edit section: Page Title">edit</a><span class="mw-editsection-bracket">]</span></span></h
1>
<p>Hello, I am some <b>bold text</b> and some <i>italic text</i>.</p>


<!--
NewPP limit report
Parsed by mw2123
Cached time: 20170425032456
Cache expiry: 2592000
Dynamic content: false
```

# Other Options

Use `-h` to view the various options at the command line.

By default, the script uses the main Wikipedia API at `https://en.wikipedia.org/w/api.php`, but this can be changed by supplying an alternate API URL with the `--apiurl` switch. (other APIs are listed [here](https://www.mediawiki.org/wiki/API:Main_page).
