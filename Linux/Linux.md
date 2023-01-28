## Linux

### Debian

<br />

##### Debian 大版本更新
##### Debian Upgrade

<br />

###### 更新现有系统
###### Update current OS
```
apt update && apt upgrade -y
```

###### 系统清理
###### Clean
```
apt --purge autoremove
```

###### /etc/apt/sources.list 文件更新为新版系统地址
###### Update /etc/apt/sources.list to new version OS
```
deb https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye main contrib non-free
# deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye main contrib non-free

deb https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye-updates main contrib non-free
# deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye-updates main contrib non-free

deb https://mirrors.tuna.tsinghua.edu.cn/debian-security bullseye-security main contrib non-free
# deb-src https://mirrors.tuna.tsinghua.edu.cn/debian-security bullseye-security main contrib non-free
```

###### 执行更新
###### Start Upgrade
```
apt update && apt full-upgrade
```

###### 验证
###### Validate
```
cat /etc/os-release
```

<br /><br />

### IUS yum源
### IUS yum sources

##### 快捷安装
##### Install
```
wget http://dl.iuscommunity.org/pub/ius/stable/Redhat/5/x86_64/ius-release-1-2.ius.el5.noarch.rpm
wget http://dl.iuscommunity.org/pub/ius/stable/Redhat/5/x86_64/epel-release-1-1.ius.el5.noarch.rpm
rpm -Uvh ius-release*.rpm epel-release*.rpm
```

##### yum包信息
##### IUS packages List

```
https://dl.iuscommunity.org/pub/
```

##### 打开/关闭显示器
##### Open/Close display
```
xset -display :0 dpms force on
xset -display :0 dpms force off
```

##### Xdotool
```
export DISPLAY=:0; xdotool key Return
```

##### 压缩
##### File compress
```
tar
解包/decompress tar xvf your_file_name.tar
打包/compress tar cvf your_file_name.tar path_name

gz
解压/decompress gunzip your_file_name.gz
解压/decompress gzip -d your_file_name.gz
压缩/compress gzip your_file_name

tar.gz
解压/decompress tar zxvf your_file_name.tar.gz
压缩/compress tar zcvf your_file_name.tar.gz path_name

zip
解压/decompress unzip your_file_name.zip
压缩/compress zip your_file_name.zip path_name
```

##### Skip SSL 证书检查
##### Skip certificate check
```
wget --no-check-certificate https://your-domain.com
curl -k https://your-domain.com
```

##### SSH Key 生成
##### SSH Key generate
```
ssh-keygen -t rsa -b 1039 -C "dvpr@me.com"
```

##### DD 硬盘克隆
##### DD command clone a disk

```
dd if=/dev/sda of=/root/output.img status=progress conv=notrunc,noerror bs=8M
```

### Linux 监控命令

##### 查看Apache连接数
##### List Apache connections

```
watch -n 1 -d "pgrep httpd|wc -l"
```

##### 查看MySQL连接数
##### List MySQL connections

```
mysqladmin -uuser -p processlist
mysqladmin -uuser -p status
```

### Linux 命令备忘
### Linux commands

##### ubuntu解压zip文件乱码
##### unzip setting character encoding

```
unzip -O CP936 xxx.zip (用GBK, GB18030也可以)
```

##### du 显示隐藏目录
##### du show hidden files

```
du -sch .[!.]* * | sort -h
```

##### SSH 代理转发
##### SSH Proxy

```
ssh -N -D1088 root@8.211.161.160
```

### 生成 SSH key
### Generate SSH key

```
ssh-keygen -t rsa -C "your_email_address"
```
