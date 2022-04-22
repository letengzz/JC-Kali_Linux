# 提高权限到root

​	自kali更新到2020版后，默认取消了root用户的登录权限。只能用普通用户登录，这样做的优点在于对于kali的新手，在不懂的部分命令的情况下对系统的损害有所降低，也就说安全性提高了。但是普通用户权限实在太低，习惯了root权限的我们在2020中如何设置登录密码呢？

```shell
kali 2020 root password
```

​	重启系统，进入下面这个界面时按`E`

![2.png](https://aimg8.dlssyht.cn/u/1809640/ueditor/image/905/1809640/1593853418182408.png)

进入此界面按`E`

按↓到`linux`开头的一行。

![3.png](https://aimg8.dlssyht.cn/u/1809640/ueditor/image/905/1809640/1593853443455163.png)

修改`ro quiet splash`为`rw quiet splash init=/bin/bash`

![4.png](https://aimg8.dlssyht.cn/u/1809640/ueditor/image/905/1809640/1593853464722947.png)

按`F10`保存后进入单用户模式

执行`passwd root`命令修改密码

![5.png](https://aimg8.dlssyht.cn/u/1809640/ueditor/image/905/1809640/1593853483572665.png)

然后重启，便可以用root身份登录了！