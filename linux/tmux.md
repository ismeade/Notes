## Tmux

### 会话

- 新建会话  
```
$ tmux new -s 会话名称  
```

- 分离会话  
会话将在后台运行
```
$ tmux detach
# 或
<C-b> d
```
<kbd>Ctrl</kbd>+b d

- 会话列表  
```shell
$ tmux ls

# 可以通过这个命令直接选择会话进入
<C-b> s
```

- 接入会话  
```
$ tmux attach -t 编号

$ tmux attach -t 会话名称
```

- 关闭会话  
```
$ tmux kill-session -t 编号

$ tmux kill-session -t 会话名称
```

- 重命名会话  
```
$ tmux rename-session -t 0 会话名称

<C-b> $
```

### 窗口

- 新建窗口  
```
$ tmux new-window

$ tmux new-window -n 窗口名称

<C-b> c
```

- 切换窗口  
```
$ tmux select-window -t 窗口编号

$ tmux select-window -t 窗口名称

<C-b> p
<C-b> n
<C-b> 窗口编号
# 通过列表选择，这里可以选择所有会话中的窗口
<C-b> w
<C-b> n
```

- 重命名窗口  
```
$ tmux rename-window 窗口名称

<C-b> ,
```

### 窗格

- 新建窗格   
```
# 上下
$ tmux split-window
<C-b> "

# 左右
$ tmux split-window -h
<C-b> %

```

- 切换窗格  
```
# 上
$ tmux select-pane -U

# 下
$ tmux select-pane -D

# 左
$ tmux select-pane -L

# 右
$ tmux select-pane -R

<C-b> 方向键
# 上一个窗格
<C-b> ;
# 下一个窗格
<C-b> o
```

- 交换窗格位置  
```
# 当前窗格上移，没有上一个时向左
$ tmux swap-pane -U
<C-b> <C-o>

# 当前窗格下移，没有下一个时向右
$ tmux swap-pane -D
<C-b> <A-o>
```

- 关闭窗格
```
<C-b> x
```

- 其他窗格操作  
```
# 将窗格移动到心=新窗口
<C-b> !
# 当前窗格全屏，再次执行回复
<C-b> z
# 调整窗格比例
<C-b> <C-方向键>
# 显示当前窗格编号
<C-b> q
```
