# shell是什么？

#### 简介

这里所说的shell也就是Linux下的终端，在Windows下的powershell与之类似，它也可以使用Linux的命令。

| 使用 | 操作 |
| :---: | :---: |
| 查看命令历史记录 | 使用上下方向键 |
| 复制 | 长按鼠标左键选中文本并拖动 |
| 粘贴 | 按鼠标中键 |

Ctrl-C和Ctrl-V是Windows下的复制粘贴命令，但shell比Windows出现的早，这两个命令有其特定含义。

#### 简单命令

| 使用 | 操作 |
| :---: | :---: |
| 查看当前系统时间和日期 | date |
| 显示当月的日历 | cal |
| 查看当前磁盘可用空间 | df |
| 显示内存 | free |
| 关闭终端窗口 | exit |

![](http://image-liypo.test.upcdn.net/Blog_Picture/%E6%BC%94%E7%A4%BA1.jpg)

#### 关机、重启与用户登录和注销

**关机和重启命令**

```bash
shutdown
    shutdown -h now:立即关机
    shutdown -h 1:1分钟后关机
    shutdown -r now:立即重启
halt:关机
reboot:重启系统
sync:把内存的数据同步到磁盘中，关机或重启前先执行这一步，防止数据丢失
```

**用户登录和注销**

1.登录时一般使用普通用户登录，尽力避免使用root账号登录，因为root是系统管理员，有最大的权限，操作不当可能误删掉核心文件。

2.在提示符下输入`logout`即可注销用户。

logout注销指令在图形运行级别无效，在运行级别3下有效。即在Linux终端中无法使用logout指令，在putty连接到Linux后，可以使用logout。

```bash
系统的运行级别配置文件/etc/inittab
运行级别0：系统停机状态，系统默认运行级别不能设为0，否则不能正常启动 
运行级别1：单用户工作状态，root权限，用于系统维护，禁止远程登陆 
运行级别2：多用户状态(没有NFS) 
运行级别3：完全的多用户状态(有NFS)，登陆后进入控制台命令行模式 
运行级别4：系统未使用，保留 
运行级别5：X11控制台，登陆后进入图形GUI模式 
运行级别6：系统正常关闭并重启，默认运行级别不能设为6，否则不能正常启动
```

