# kali2020.2设置中文

1. 先更新源`vi /etc/apt/sources.list`

![1.png](https://aimg8.dlssyht.cn/u/1809640/ueditor/image/905/1809640/1593854174553045.png)

更新源

```shell
#中科大
deb http://mirrors.ustc.edu.cn/kali kali-rolling main non-free contrib
deb-src http://mirrors.ustc.edu.cn/kali kali-rolling main non-free contrib
  
#阿里云
deb http://mirrors.aliyun.com/kali kali-rolling main non-free contrib
deb-src http://mirrors.aliyun.com/kali kali-rolling main non-free contrib
  
#清华大学
deb http://mirrors.tuna.tsinghua.edu.cn/kali kali-rolling main contrib non-free
deb-src https://mirrors.tuna.tsinghua.edu.cn/kali kali-rolling main contrib non-free
  
#浙大
deb http://mirrors.zju.edu.cn/kali kali-rolling main contrib non-free
deb-src http://mirrors.zju.edu.cn/kali kali-rolling main contrib non-free
  
#东软大学
deb http://mirrors.neusoft.edu.cn/kali kali-rolling/main non-free contrib
deb-src http://mirrors.neusoft.edu.cn/kali kali-rolling/main non-free contrib
```

2. 更新软件

```shell
apt-get update && apt-get upgrade && apt-get clean
```

![2.png](https://aimg8.dlssyht.cn/u/1809640/ueditor/image/905/1809640/1593854239543338.png)

3. 选择编码

```shell
dpkg-reconfigure locales
```

然后选择字符编码： `en_US.UTF-8`、`zh_CN.GBK`、`zh_CN.UTF-8` （用空格选定）选定后按一下TAB键 到OK然后空格就ok！

回车键下一步

回车键进入下一步

![3.png](https://aimg8.dlssyht.cn/u/1809640/ueditor/image/905/1809640/1593854270456425.png)

4. 选择`zh_CN.UTF-8`

​	回车进入下一步

![4.png](https://aimg8.dlssyht.cn/u/1809640/ueditor/image/905/1809640/1593854291684350.png)

5. 安装中文字体

```
sudo apt-get install ttf-wqy-microhei ttf-wqy-zenhei xfonts-wqy
```

![5.png](https://aimg8.dlssyht.cn/u/1809640/ueditor/image/905/1809640/1593854325151947.png)

6. 最后一步重启系统即可

​	reboot

![6.png](https://aimg8.dlssyht.cn/u/1809640/ueditor/image/905/1809640/1593854347176836.png)

**不得不提一点有些小伙伴装了kali2020.1或2020.2后发现类似ifocnfig与reboot之类的命令用不了 其实这个情况手动重启一下kali就好了**