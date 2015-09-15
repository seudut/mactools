title: Linux Tool on Mac
speaker: Peng Li
url: https://github.com/seudut/mactool.git
transition: move
files: /js/demo.js,/css/demo.css,/js/zoom.js
theme: dark
<!-- 
1. 这些都不是我自己的，都是从网上别人开发的工具，都是开源，免费的
2. 都是一些最基本的概念， 没有什么技术含量, 一是我自己懂得的也不多，不太会讲，二时
时间不够，大多数需要自己去练习。
3. 其中很多个人自定的，也许只适合自己，仅供大家参考
Powered By nodePPT [](https://github.com/ksky521/nodePPT)
-->

[slide]
## Agenda
---
* Efficient Tools on Mac/Unix (command line) {:&.rollIn}
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

    * find file with file name {:&.rollIn}
      <pre><code class="bash">$ ag -sg 'SessionImpl' ./cpve</code></pre>
      equal: <pre><code class="bash">$ find ./cpve -name '*SessionImpl*'</code></pre>
    * find word in files
      * <pre><code class="bash">$ ag -s 'send_scr' ./</code></pre>
      * <pre><code class="bash">$ ag 'send_scr' ./ --ignore-dir target/</code></pre>
    * search keywork with filetype
      * <pre><code class="bash">$ ag 'send_scr' . --cc</code></pre>
      * <pre><code class="bash">$ ag 'iosversion' --python </code></pre>
  * integrated in vim, plugin ack.vim

[slide]

* 7zip {:&.rollIn}
    <pre><code class="bash">$ brew install p7zip</code></pre>
* wget, lftp - clients for http and ftp
  * <pre><code class="bash">$ brew install wget</code></pre>
  * <pre><code class="bash">$ brew install lftp</code></pre>
  * demo lftp-cp and 7z

    transfer local file to cmbu-ftp
  * <pre><code class="bash">$ lftp-cp local_file remote_file </code></pre>

* two tools for Key Remap on Mac keyboard
  * Karabiner - <https://pqrs.org/osx/karabiner/>
  * Seil - <https://pqrs.org/osx/karabiner/seil.html.en>
  * remap Caps Lock to Ctrl/Esc
* tmux + vim + zsh for programming 

[slide]

# Shortcuts on bash - command line
* motion {:&.rollIn}
  * Ctrl+A, Ctrl+E
  * Ctrl+B, Ctrl+F, 
  * Alt+b, Alt+f
  * Ctrl+L
* Yank & Paste
  * Ctrl+K, Ctrl+U, Ctrl+Y
  * Ctrl+D, Alt+d, Ctrl+W

[slide]

* history Command {:&.rollIn}
  * Ctrl+P, Ctrl+N
  * Ctrl+R
  * !N, !!, - run command in history

* Job break
  * Ctrl+C
  * Ctrl+Z

* TAB completion 
  * use TAB completion as much as possible
  * replace Zsh with bash, TAB completion in zsh is much better 
    <pre><code class="bash">$ chsh -s /bin/zsh</code></pre>

[slide]

# other commands
* cd; cd - ; cd ~ {:&.rollIn}
* scp 
  * more convenient than USB flash copy and ftp transfer
  * examples
     <pre><code class="bash">$ scp localfile peli3-imac@10.140.112.160:temp/</code></pre>
     <pre><code class="bash">$ scp peli3-imac@10.140.112.160:temp/remotefile ./localfile</code></pre>
     <pre><code class="bash">$ scp -r local_dir peli3-imac@10.140.112.160:temp/</code></pre>
* SSH vs VNC
  * demo build CPVE android/Linux on remote VM
* combine multiple command - && or pipe
 
  * Example:  merge multiple jabber log

    <pre><code type="bash">$ ls -rl jabber.log*  | awk '{print $9}' | Xargs cat >> full.log</code></pre>

* An interesting page for unix command vote [commandlinefu](http://www.commandlinefu.com/commands/browse/sort-by-votes)

[slide]

# Vim Basic
* [Vim](http://www.vim.org/) vs [Emacs](https://www.gnu.org/software/emacs/), [sublime Text](http://www.sublimetext.com/), [atom](https://atom.io/) {:&.rollIn}
  * Open Source, no license, free, cross-platforms
  * Plug-Ins
  * vim is modal editing editor
  * vim shorter key mapping
  * vim is default editor on Linux server or even embedded development 

* Install Macvim to replace with default vim
    * <pre><code class="bash">$ brew install macvim</code></pre>

* modal editing, four main modes
  * *Normal mode* `Esc` -  motion and edit
  * Visual mode - select and copy `v`
  * Insert mode - input text `i, a, o`
  * Command-line mode - execute command `:`

[slide]

* Normal Mode
  * input `<Esc>` to Normal mode
  * motion
    * h, j, k, l
    * e, w, b, f, {, } 
    * C-B, C-F, C-U, C-D
    * f, t
  * change
    * delete `x, d,`
    * Yank & Paste `y, p`
    * Undo & Redo `u, C-R`
  * Text Objects
    * word
    * sentence
    * line
    * paragraph
    * example: `viw` `vaw` `ciw` `diw` `yaw`

[slide]
# other concept
* Buffer {:&.rollIn}
  * <pre><code class="vim">:help buffers<CR></code></pre>

* Window
  * <pre><code class="vim">:help windows<CR></code></pre>
* Tab
* Registers
* Marks

[slide]

# vimrc - config file
  
  vim is hard to use without any config - `~/.vimrc`
  
* Using default `vimrc_example.vim` to `~/.vimrc`  {:&.rollIn}

  <pre><code class="vim">:!cp $VIMRUNTIME/vimrc_example.vim ~/.vimrc</code></pre>

  or 

  <pre><code class="bash">$ cp /usr/local/Cellar/macvim/7.4-73_1/MacVim.app/Contents/Resources/vim/runtime/vimrc_example.vim ~/.vimrc</code></pre>

* Key Mapping
  * `nmap cmap vmap`
  * mapping 'jj' to Esc

* Plugins
  * plug-in manager
    * [Vundle](https://github.com/VundleVim/Vundle.vim)
  * [vim awesome](http://vimawesome.com/) - A page for most popular vim plugins

[slide]

# some tips

* Use `:help` for any document {:&.rollIn}
  * <pre><code class="vim">:help h</code></pre>
  * <pre><code class="vim">:help Normal</code></pre>
  * <pre><code class="vim">:help map</code></pre>

* Stay in Normal mode as much as possible
  * Insert mode is the weakest mode
  * most time we are 

* Never use arrow key, Use h j k l, C-F, C-B, C-U, C-D in Normall mode

* [vim wiki tips](http://vim.wikia.com/wiki/Vim_Tips_Wiki)

  you can find lots of tips of usage of vim

* [vim cheat sheel](http://www.viemu.com/a_vi_vim_graphical_cheat_sheet_tutorial.html)

[slide]

# demo

* vim for the first c program {:&.rollIn}

* vim for C/C++ environment 
  * suggest plugins
    * FuzzyFinder or Ctrlp or CommandT
    * ctags - Exuberant Ctags
    * gtags - gnu global
    * Easymotion
    * YouCompleteMe
  * [vim awesome](http://vimawesome.com/) - for more plugins, Screen shot or demo on youtube

* Vimperator - an Firefox Add-ons with Vim shortcuts

[slide]

# RegExp for Log 

<!--  most command tool and text editor support regular expressions, using regexp can search what we want more quickly -->
  most editor and command support regular expressions

* regular expression vs. wildcards {:&.rollIn}
  * `*` can be a wildcard or a meta character in regexp depend on the context or the command 

* Simple patterns
  * Metacharacters
    * `.` - dot, any single character except a newline
    * `*` - star, match preceding item zero or more times
    * `+` - plus, match preceding iterm one or more time

    `.*` match any character any number of times

  * Alternatives `|`  or
  * group `()`
  * class `[]`
  * `^ $ \s \d \w`

* Usage Sample - CPVE logs 
