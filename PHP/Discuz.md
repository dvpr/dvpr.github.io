## Discuz

### 修改创始人密码

1.	在网站根目录下的子目录uc_server/data中找到文件config.inc.php，打开它，找到类似以下代码：

```
define('UC_FOUNDERPW', '256955f2e034sad74f0e2953572ea360');
define('UC_FOUNDERSALT', '217804');
```

2.	然后用以下代码替换上述代码：

```
define('UC_FOUNDERPW', '047099adb883dc19616dae0ef2adc5b6');
define('UC_FOUNDERSALT', '311254');
```

3.	修改完后，Ucenter创始人的密码就变为: 123456789　

### Discuz X 开启防CC攻击

在config/config_global.php文件中有如下代码：

```
$_config['security']['attackevasive']        = 0;
```

可以设置的值有：

> 0表示关闭此功能  
> 1表示cookie刷新限制  
> 2表示限制代理访问  
> 4表示二次请求  
> 8表示回答问题（第一次访问时需要回答问题）

同时也可以设置为组合的方式：

> 如1|2表示同时启用cookie刷新限制和限制代理访问。
