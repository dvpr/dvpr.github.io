## Linux

### IUS yum源

##### 快捷安装

```
wget http://dl.iuscommunity.org/pub/ius/stable/Redhat/5/x86_64/ius-release-1-2.ius.el5.noarch.rpm
wget http://dl.iuscommunity.org/pub/ius/stable/Redhat/5/x86_64/epel-release-1-1.ius.el5.noarch.rpm
rpm -Uvh ius-release*.rpm epel-release*.rpm
```

##### yum包信息

```
https://dl.iuscommunity.org/pub/
```

### Linux 监控命令

##### 查看apache连接数

```
watch -n 1 -d "pgrep httpd|wc -l"
```

##### 查看MySQL连接数

```
mysqladmin -uuser -p processlist
mysqladmin -uuser -p status
```
