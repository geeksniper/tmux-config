# tmux-config

Config from [ippsec](https://www.youtube.com/watch?v=Lqehvpe_djs).
```
#set prefix
set -g prefix C-a
bind C-a send-prefix
unbind C-b

set -g history-limit 100000
set -g allow-rename off

bind-key j command-prompt -p "Join pan from:" "join-pane -s '%%'"
bind-key s command-prompt -p "Send pane to:" "joian-pane -t '%%'"

set-window-option -g mode-keys vi

run-shell /opt/tmux-logging/logging.tmux

```

First press the prefix `ctrl + a`, *then* release the buttons and press the combination you want.

`tmux new -s [Name]`

new named session

`prefix + c`

create new window

`prefix + ,`

Rename window

`prefix + #`

change panes

`prefix + w`

list windows

`prefix + % `

vertical split

`prefix + "`

horizontal split

`prefix + s #`

join pane

`prefix + z`

zoom in/out to panes 

`prefix + !`

make splitted part to own window

`prefix + ]`

enter vim mode
-> search with `?` in vi mode
-> press `space` to start copying
-> press `prefix + ]` to paste

`alt + .`

cycle through arguments in history

`tmux kill-session -t X`

kill session by tag

`prefix + &`

kill pane










