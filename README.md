# Linux settings (how to use)
```
cd
git clone https://github.com/knmac/linux_settings.git
cp linux_settings/vimrc/* .
cp linux_settings/tmux/* .
rm -r linux_settings
```


# vimrc's installation guide
## Required packages
```
sudo apt-get install curl vim exuberant-ctags git ack-grep
sudo pip install pep8 flake8 pyflakes isort yapf
```

## Cheatsheet
Some self-defined shortcuts (in normal mode)
* Open todo list: F2
* Navigate between files and folders: F3
* Navigate between functions: F8
* Open error list: F9
* Open tab manager: tl
* Quick command: \ci
* Go to definition: ,d
* Go to assignment: ,a
* Find occurences: ,o
* Auto complete (in editor mode): Ctrl + space
* Search files: Ctrl + P

Some useful vim shortcuts:
* Line navigation:
    * h, j, k, l: left, down, up, right
    * 0, $: start / end of current line
    * ^, g\_: non-blank start / end of current line
* Text navigation:
    * w, b: next / previous beginning of a word
    * e: end of a word
* Screen navigation:
    * gg, G: first / last line
    * nG (or :n): go to n'th line
    * Ctrl-U, Ctrl-D: half-page up / down
* Search navigation:
    * :/[pattern]: search for pattern
    * n, N: next / previous matching pattern
* Window navigation:
    * :split: horizontal split
    * :vsplit: vertical split
    * Ctrl+w [h/j/k/l]: move to left/ down/ up/ right window
* Code folding:
    * za: toggle folding
* Open multiple files with buffer: (can be combined with NERDTree and CtrlP)
    * :badd [filename]: open file in new buffer
    * :bn: next buffer
    * :bp: previous buffer
    * :bd: delete buffer
    * :ls: list all buffer
    * :b [number / filename]: go to that buffer


# tmux 2.4's installation guide
## Install from source (filename and link may change over time)
```
sudo apt-get update
sudo apt-get install -y libevent-dev libncurses-dev make
wget https://github.com/tmux/tmux/releases/download/2.4/tmux-2.4.tar.gz
tar xvzf tmux-2.4.tar.gz
cd tmux-2.4/
./configure && make
sudo make install
```

## Cheat sheet
(After pressing Ctrl - b)
* Mouse mode: m
* Split veritcally: |
* Split horizontally: -
* Create new window: c
* Kill pane: x
* Kill window: &
* Navigate, resize: use your mouse :)
* Copy mode:
  * Start copy mode: Ctrl-b Enter
  * Select with mouse
  * Paste from buffer: Ctrl-b p
  * List buffer: Ctrl-b b
  * Choose buffer: Ctrl-b P
