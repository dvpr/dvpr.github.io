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

##### 暂存并推出会话
##### Detach tmux
```
Ctrl + b d
```

##### Pane 进入全屏
##### Pane enter full screen
```
Ctrl + b z
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