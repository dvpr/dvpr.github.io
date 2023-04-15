## Tmux
> 终端多窗口神器

<br /><br />

### 默认快捷键前缀
### Default prefix key
```
Ctrl + b
```

<br />

##### 列出会话
##### List sessions
```
tmux ls
```

<br />

##### 暂存并退出会话
##### Detach tmux
```
Ctrl + b d
```

<br />

##### 重新进入会话
##### Attaches to an existing session
```
tmux attach -t <session-name>
```

<br />

##### 拆分窗口
##### Splitting the window
```
Ctrl + b % (横向拆分/splits the current pane into two horizontally)
Ctrl + b " (纵向拆分/splits the current pane into two vertically)
```

<br />

##### Pane间切换
##### The active pane changed between the panes in a window
```
Ctrl + b q (显示Pane编号/prints the pane numbers)
Ctrl + b q <number> (切换到指定编号Pane/change to pane number)
```

<br />

##### Pane移动
##### Move pane
```
Ctrl + b { (先前移动/forward)
Ctrl + b } (先后移动/backward)
```

<br />

##### 新建Window
##### Create new window
```
Ctrl + b c
```

<br />

##### Window间切换
##### The active window changed between the windows
```
Ctrl + b <number>
```

<br />

##### Pane 进入全屏
##### Pane enter full screen
```
Ctrl + b z
```

<br />

##### 进入复制模式 - 游走于历史输出中
##### Enter copy mode
```
Ctrl + b [
```

<br />

### Tmux 命令进入命令行模式
### Tmux enter command mode
```
Ctrl + b :
```

<br />

### 禁用window重命名
### disable window automatic-rename
```
set-window-option -g automatic-rename off
```

<br />

##### Pane 调整大小
##### Resize pane
```
:resize-pane -D (向下拉伸/Resizes the current pane down)
:resize-pane -U (向上拉伸/Resizes the current pane upward)
:resize-pane -L (向左拉伸/Resizes the current pane left)
:resize-pane -R (向右拉伸/Resizes the current pane right)
:resize-pane -D 10 (向下拉伸10个单位/Resizes the current pane down by 10 cells)
:resize-pane -U 10 (向上拉伸10个单位/Resizes the current pane upward by 10 cells)
:resize-pane -L 10 (向左拉伸10个单位/Resizes the current pane left by 10 cells)
:resize-pane -R 10 (向右拉伸10个单位/Resizes the current pane right by 10 cells)
```