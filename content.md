title: Linux Tool on Mac
speaker: Peng Li
url: https://github.com/seudut/mactool.git
transition: move
files: /js/demo.js,/css/demo.css,/js/zoom.js
theme: dark
<!-- 
这些都不是我自己的，都是从网上别人开发的工具，都是开源，免费的

没有什么技术含量
Powered By nodePPT [](https://github.com/ksky521/nodePPT)
-->

[slide]
# Contens
## Test
<small> Peng Li </small>

# 样式展示 {:&.flexbox.vleft}
> nodePPT 让每个人都爱上做分享！

[slide]
## Agenda
---
* Efficient Tools on Mac (command line) {:&.rollIn}
* Shortcut Key on bash/zsh
* Vim Basic
* RegExp Basic

[slide]

# Efficient Tools
* [Homebrew](http://brew.sh/) - package manager for OSX {:&.rollIn}
 * Install <http://brew.sh/>

    <pre><code class="ruby">ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"</code></pre>
 
 * options
   * <pre><code class="ruby">brew search pkg_name</code></pre> 
   * <pre><code class="ruby">brew install pkg_name</code></pre> 

 * Auther: Max Howell 
 * vs apt-get, yum on Linux

[slide]

* [Quicksilver](http://qsapp.com/)  - Applecation Launcher 
 * Open Source on [github](https://github.com/quicksilver/Quicksilver), no license 
 * [User Guide](http://qsapp.com/wiki/Quicksilver_User's_Guide)
 * Fuzzy matching
 * Launch App
 * Open File/Directory
 * support AppleScript 
   * hotkey to toggle applecation
 * alternative -  [Alfred](https://www.alfredapp.com/)

[slide]

<!-- # Tools on Commond Line (Cont.) -->
<!-- * [the\_silver\_searcher](http://geoff.greer.fm/ag/) a tool for searching code - Ag {:&.rollIn}-->
* [the\_silver\_searcher](http://geoff.greer.fm/ag/) a tool for searching code - Ag

 * Install

     <pre><code class="ruby">brew install the_silver_searcher</code></pre>

 * vs Grep/Ack/Ag
   * faster than ack, grep
   * ignore files in .git .svn

   ![Alt text](/ag_grep.png)

[slide]

* [the\_silver\_searcher](http://geoff.greer.fm/ag/) a tool for searching code - Ag

 * Usage 

    * find file with file name 
      <pre><code class="bash">$ ag -sg 'SessionImpl' ./cpve</code></pre>
      equal: <pre><code class="bash">$ find ./cpve -name '\*SessionImpl\*'</code></pre>
    * find word in file
      <pre><code class="bash">$ ag -s 'send_scr' ./</code></pre>
      <pre><code class="bash">$ ag 'send_scr' ./ --ignore-dir target/</code></pre>
    * search keywork with filetype
      <pre><code class="bash">$ ag 'send_scr' . --cc</code></pre>
      <pre><code class="bash">$ ag 'iosversion' --python </code></pre>

[slide]

* 7zip
    <pre><code class="bash">$ brew install p7zip</code></pre>
* wget lftp
  * scripting with ftp client
  * example with lftp-cp and 7z

[slide]

* Karabiner - <https://pqrs.org/osx/karabiner/>
* Seil - <https://pqrs.org/osx/karabiner/seil.html.en>

[slide]

# Shortcuts on bash - command line
* motion 
  * Ctrl+A
  * Ctrl+E
  * Ctrl+B, Alt+b
  * Ctrl+F, Alt+f
* Yank & Paste
  * Ctrl+L, Ctrl+W, Ctrl+K, Ctrl+U, Ctrl+Y
  * Ctrl+D, Alt+d
* History
  * Ctrl+R 
* Ctrl+P, Ctrl+N

* Job break
  * Ctrl+C
  * Ctrl+Z

[slide]

* replace Zsh with bash
  <pre><code class="bash">$ chsh -s /bin/zsh</code></pre>
  * advantage: 

# short commands
* cd; cd - ; cd ~/
* zsh 

*  command full
<http://www.commandlinefu.com/commands/browse/sort-by-votes>
 * grep/sed/awk/perl

    ls -rl jabber.log*  | awk '{print $9}' | Xargs cat >> full.log

[slide]
## Key remap for MacBook
* Karabiner
* Seil
* remap Caps Lock to Ctrl
* command 
 *  command full
<http://www.commandlinefu.com/commands/browse/sort-by-votes>
 * cd ; cd - ; cd ~
 * grep/sed/awk/perl

    ls -rl jabber.log*  | awk '{print $9}' | Xargs cat >> full.log

[slide]
## percol

# Vim Basic
## Macvim
* Vim vs Emacs
* :help
* modal editing, four main modes
  * Normal mode
  * Visual mode
  * Insert mode
  * Command-line mode

* switch mode, <Esc>, i, v

* Normal Mode
  * motion
    * h, j, k, l
    * C-B, C-F, C-U, C-D
    * f, t
  * change
    * x, d, 
    * y, p
    * u, C-R

* Never using arrow key

* stay in Normal mode as much as possible
  Insert mode is the weakest mode
* [Seven habits of effective text editing](http://www.moolenaar.net/habits.html)


* step by step
* plugin package manager
* vimrc example
* first c program

* Vimperator - Firefox

## tmux + zsh + vim

# RegExp for Log 
* regular expression vs. wildcards
* this is the firsit
