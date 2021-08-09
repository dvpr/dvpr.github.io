## Tmux
## 终端多窗口神器

### Default prefix key
### 默认快捷键前缀
```
Ctrl + b
```

##### Pane enter full screen
##### Pane 进入全屏
```
Ctrl + b z
```

### Tmux enter command mode
### Tmux 命令进入命令行模式
```
Ctrl + b :
```

##### Resize pane
##### Pane 调整大小
```
:resize-pane -D (Resizes the current pane down/向下拉伸)
:resize-pane -U (Resizes the current pane upward/向上拉伸)
:resize-pane -L (Resizes the current pane left/向左拉伸)
:resize-pane -R (Resizes the current pane right/向右拉伸)
:resize-pane -D 10 (Resizes the current pane down by 10 cells/向下拉伸10个单位)
:resize-pane -U 10 (Resizes the current pane upward by 10 cells/向上拉伸10个单位)
:resize-pane -L 10 (Resizes the current pane left by 10 cells/向左拉伸10个单位)
:resize-pane -R 10 (Resizes the current pane right by 10 cells/向右拉伸10个单位)
```