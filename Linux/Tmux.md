## Tmux
## 终端多窗口神器

### 默认快捷键前缀
### Default prefix key
```
Ctrl + b
```

##### 列出会话
##### List sessions
```
tmux ls
```

##### 暂存并退出会话
##### Detach tmux
```
Ctrl + b d
```

##### 重新进入会话
##### Attaches to an existing session
```
tmux attach -t <session-name>
```

##### 拆分窗口
##### Splitting the window
```
Ctrl + b % (横向拆分/splits the current pane into two horizontally)
Ctrl + b " (纵向拆分/splits the current pane into two vertically)
```

##### Pane间切换
##### The active pane changed between the panes in a window
```
Ctrl + b q (显示Pane编号/prints the pane numbers)
Ctrl + b q <number> (切换到指定编号Pane/change to pane number)
```

##### 新建Window
##### Create new window
```
Ctrl + b c
```

##### Window间切换
##### The active window changed between the windows
```
Ctrl + b <number>
```

##### Pane 进入全屏
##### Pane enter full screen
```
Ctrl + b z
```

##### 进入复制模式
##### Enter copy mode
```
Ctrl + b [
```

### Tmux 命令进入命令行模式
### Tmux enter command mode
```
Ctrl + b :
```

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