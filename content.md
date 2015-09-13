title: Linux Tool on Mac
speaker: Peng Li
url: https://github.com/seudut/mactool.git
transition: move
files: /js/demo.js,/css/demo.css,/js/zoom.js
theme: dark
<!-- 
这些都不是我自己的，都是从网上别人开发的工具，都是开源，免费的
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
* Tools on Commond Line {:&.rollIn}
* Shortcut Key on Command Line
* Vim Basic
* RegExp Basic

[slide]

# Tools on Commond Line
* [Homebrew](http://brew.sh/) - package manager for OSX {:&.rollIn}
 * Install

    <pre><code class="ruby">ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"</code></pre>
 
 * options
   * <pre><code class="ruby">brew search pkg_name</code></pre> 
   * <pre><code class="ruby">brew install pkg_name</code></pre> 

 * Auther: Max Howell 
 * vs apt-get, yum on Linux

[slide]

# Tools on Commond Line (Cont.)
<!-- * [the\_silver\_searcher](http://geoff.greer.fm/ag/) a tool for searching code - Ag {:&.rollIn}-->
* [the\_silver\_searcher](http://geoff.greer.fm/ag/) a tool for searching code - Ag

 * Install

     <pre><code class="ruby">brew install the_silver_searcher</code></pre>

 * vs Grep/Ack/Ag
   * faster than ack, grep
   * ignore files in .git .svn

   ![Alt text](/ag_grep.png)


 * Usage - example
    * find file with file name 
      <pre><code class="bash">ag -sg 'SessionImpl' ./cpve</code></pre>
    * find word in file
      <pre><code class="bash">ag -s 'send_scr' ./</code></pre>
      <pre><code class="bash">ag 'send_scr' ./ --ignore-dir target/</code></pre>
    * search keywork with filetype
      <pre><code class="bash">ag 'send_scr' . --cc</code></pre>



[slide]

* 7zip, zip/unzip, unrar
* wget lftp
* iTerm2
* tmux + macvim + 
## tools
* Quicksilver  - Afred
 * AppleScript
* Karabiner - <https://pqrs.org/osx/karabiner/>
* Seil - <https://pqrs.org/osx/karabiner/seil.html.en>

[slide]

# Shortcut Key on Commands Line
* Ctrl +
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

## percol

# Vim Basic
* Macvim
* Vimperator - Firefox

## tmux + zsh + vim

# RegExp for Log 
* regular expression vs. wildcards
