##cPanel

### 无法登录WHM

关闭cPHulk

```
for i in `ps aux | grep -i "cphulkd - process" | awk {'print $2'}` ;do kill -9 $i ;done
/usr/local/cpanel/bin/cphulk_pam_ctl --disable
```

### Can't enable SMTP Restrictions

```
/scripts/smtpmailgidonly on
```
