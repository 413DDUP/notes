<!---title:设置CentOS启动默认进入控制台而不是图形界面-->
<!---keywords:FPGA-->
<!---date:old-->

开始进行驱动程序的学习之后，发现控制台越来越方便，很少进图形界面了，因此对系统配置文件稍加修改，默认进入控制台界面。

```
# vim /etc/inittab
```

![][1]

修改，将

```
id:5:initdefault:
```

中的5改为3，如下

```
id:3:initdefault:
```

就像注释中说的，千万不要设成0或这6，1表示单用户模式，3为无x11的多用户模式，5有x11即图形界面。



[1]:../images/设置CentOS启动默认进入控制台而不是图形界面/1.jpg