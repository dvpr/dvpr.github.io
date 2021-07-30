## SNMP

### SNMP Traps

##### 开启trap接收进程

```
snmptrapd -C -c /etc/snmp/snmptrapd.conf -df -Lo
```

##### 记录tcp请求信息

```
tcpdump -i ens192 src 10.68.19.147
```

##### 手动发送Traps请求

```
snmptrap -v 1 -c public 127.0.0.1 '.1.3.6.1.6.3.1.1.5.4' '0.0.0.0' 6 33 '55' .1.3.6.1.6.3.1.1.5.4 s "eth0"
snmptrap -v 2c -c storage_public 127.0.0.1:162 '' .1.3.6.1.2.1.1.1.0 .1.3.6.1.2.1.1.1.0 s "eth1"
```

##### 手动发送snmp请求

```
snmpwalk -v 2c -c storage_public 10.68.19.147
```

华为存储系统默认只读团体字为“storage_public”，读写团体字为“storage_private”。