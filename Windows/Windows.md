## Windows

##### 清理系统图标缓存数据库脚本
##### Clean icon cache

```
rem 关闭Windows外壳程序explorer

taskkill /f /im explorer.exe

rem 清理系统图标缓存数据库

attrib -h -s -r "%userprofile%\AppData\Local\IconCache.db"

del /f "%userprofile%\AppData\Local\IconCache.db"

attrib /s /d -h -s -r "%userprofile%\AppData\Local\Microsoft\Windows\Explorer\*"

del /f "%userprofile%\AppData\Local\Microsoft\Windows\Explorer\thumbcache_32.db"
del /f "%userprofile%\AppData\Local\Microsoft\Windows\Explorer\thumbcache_96.db"
del /f "%userprofile%\AppData\Local\Microsoft\Windows\Explorer\thumbcache_102.db"
del /f "%userprofile%\AppData\Local\Microsoft\Windows\Explorer\thumbcache_256.db"
del /f "%userprofile%\AppData\Local\Microsoft\Windows\Explorer\thumbcache_1024.db"
del /f "%userprofile%\AppData\Local\Microsoft\Windows\Explorer\thumbcache_idx.db"
del /f "%userprofile%\AppData\Local\Microsoft\Windows\Explorer\thumbcache_sr.db"

rem 清理 系统托盘记忆的图标

echo y|reg delete "HKEY_CLASSES_ROOT\Local Settings\Software\Microsoft\Windows\CurrentVersion\TrayNotify" /v IconStreams
echo y|reg delete "HKEY_CLASSES_ROOT\Local Settings\Software\Microsoft\Windows\CurrentVersion\TrayNotify" /v PastIconsStream

rem 重启Windows外壳程序explorer

start explorer
```

[脚本下载](/assets/windows/clean_icon_cache.zip) ***解压后运行***

##### Thunderbird 配置文件
##### Thunderbird config on startup

```
thunderbird.exe -profilemanager
```

##### 个人版Xshell申请地址
##### Xshell Free for Non-Commercial Use Only
```
[https://www.netsarang.com/en/free-for-home-school](https://www.netsarang.com/en/free-for-home-schoo)
```
