# Linux 防火墙
# Linux Firewall

## firewalld

```
启动/Start: systemctl start firewalld
关闭/Stop: systemctl stop firewalld
查看状态/Status: systemctl status firewalld 
开机禁用/Start on boot: systemctl disable firewalld
开机启用/Stop on boot: systemctl enable firewalld

查看激活的区域/List active zones
firewall-cmd --get-active-zones

在指定区域增加服务/Add service at specific zone
firewall-cmd --zone=public --permanent --add-service=http
firewall-cmd --zone=public --permanent --add-service=https

在指定区域删除服务/Remove service at specific zone
firewall-cmd --zone=public --permanent --remove-service=ssh

新建区域并为指定IP添加端口/Create zone and add port for specific IP
firewall-cmd --new-zone=app-delivery --permanent
firewall-cmd --zone=app-delivery --add-source=59.65.196.31/32 --permanent
firewall-cmd --zone=app-delivery --add-port=8080/tcp --permanent

加载规则/Reload rules
firewall-cmd --reload
```