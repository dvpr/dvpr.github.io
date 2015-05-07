##Aliyun CentOS

###添加yum源
    rpm -Uvh http://mirror.webtatic.com/yum/el6/latest.rpm

###服务器部署记录

- #####查看信息

      cat /etc/redhat-release，查看版本
      uname -a – 显示版本和内核信息
      rpm -q kernel – 显示内核版本
      yum -y update – 升级所有应用版本，更新CentOS到最新镜像版本

- #####安装
      yum install mysql mysql-server                          //安装Mysql
      chkconfig --levels 235 mysqld on                        //Mysql开机启动
      /etc/init.d/mysqld start                                //运行mysql
      mysql_secure_installation-----------------不好使         //Mysql安装向导
      mysqladmin -u root password xx                          //设置mysql密码
      yum install httpd                                       //安装Apache
      chkconfig --levels 235 httpd on                         //Apache开机启动
      /etc/init.d/httpd start                                 //启动Apache
      访问域名
      apache preloadpage---------------干啥用啊
      yum install php/php53                                   //安装php
      /etc/init.d/httpd restart                               //重启Apache
      yum search php                                          //搜索php相关模块
      yum install php-mysql php-gd php-imap php-ldap php-odbc php-pear php-xml php-xmlrpc  //安装php模块
      /etc/init.d/httpd restart                               //重启Apache

- [VSFTP](http://wiki.centos.org/HowTos/Chroot_Vsftpd_with_non-system_users) 安装ftp

      yum install vsftpd db4-utils

  [vsftpd_virtual_config_withTLS](http://wiki.centos.org/HowTos/Chroot_Vsftpd_with_non-system_users?action=AttachFile&do=get&target=vsftpd_virtual_config_withTLS.sh) 下载配置脚本

      chkconfig --levels 235 vsftpd on
      iptables -A INPUT -m state --state NEW -m tcp -p tcp --dport 21 -j ACCEPT
      iptables -A INPUT -m state --state NEW -m tcp -p tcp --dport 64000:65535 -j ACCEPT
      vim /etc/vsftpd/vsftpd.conf  //修改主机ip
      /etc/init.d/vsftpd restart   //重启vsftp  

- #####配置FTP

  修改ftp路径
      /etc/vsftpd/users //编辑相应用户文件

###配置apache、mysql、php

- apache 配置

    ```
    #vi /etc/httpd/conf/httpd.conf
    ```

    ```
    #Servername www.example.com  80 修改为： Servername www.mglog.net  80
    ```

    (指定为你自己的域名，如果没有域名，设置为localhost)

    ```
    ServerTokens  OS  修改为： ServerTokens Prod
    ```

    (大约在44行，在出现错误页的时候不显示服务器操作系统名称)

    ```
    ServerSignature On  修改为： ServerSignature Off
    ```

    (大约在536行，在错误页中不显示Apache版本)

    ```
    --------------------Options Indexes FollowSymLinks 修改为：Options Includes ExecCGI FollowSymLinks
    ```

    (大约在在331行，允许服务器执行CGI及SSI，禁止列出目录)  

    ```
    ---------------------#AddHandler cgi-script .cgi 修改为：AddHandler cgi-script .cgi .pl
    ```

    (大约在在796行， 允许扩展名为.pl的CGI脚本运行)  

    ```
    -------------------AllowOverride None  修改为：AllowOverride All
    ```

    (大约在338行，允许.htaccess)

    ```
    -------------------AddDefaultCharset UTF-8 修改为：AddDefaultCharset GB2312
    ```

    (大约在，在759行 添加GB2312为默认编码)  

    ```
    ------------------ Options Indexes MultiViews FollowSymLinks 修改为
    ```

    (不在浏览器上显示树状目录结构，大约在554行)  

    ```
    DirectoryIndex index.html index.html.var  修 改为：DirectoryIndex index.html index.htm Default.html Default.htm index.php Default.php index.html.var
    ```

    (设置默认首页文件，增加index.php，约在在402行)  

    ```
    --------------------- KeepAlive Off 修改为：KeepAlive On
    ```

    (允许程序性联机 约在76行)  

    ```
    MaxKeepAliveRequests 100 修改为：MaxKeepAliveRequests 1000
    ```

    (增加同时连接数，约在83行)

    ```
    :wq!     #保存退出
    ```

- php配置  

    ```
    # vi /etc/php.ini
    ```

    ```
    date.timezone = PRC             #在946行 把前面的分号去掉，改为date.timezone = PRC
    ```

    ```
    disable_functions  =passthru,exec,system,chroot,scandir,chgrp,chown,shell_exec,proc_open,proc_get_status,ini_alter,ini_alter,ini_restore,dl,openlog,syslog,readlink,symlink,popepassthru,stream_socket_server,escapeshellcmd,dll,popen,disk_free_space,checkdnsrr,checkdnsrr,getservbyname,getservbyport,disk_total_space,posix_ctermid,posix_get_last_error,posix_getcwd, posix_getegid,posix_geteuid,posix_getgid,  posix_getgrgid,posix_getgrnam,posix_getgroups,posix_getlogin,posix_getpgid,posix_getpgrp,posix_getpid,  posix_getppid,posix_getpwnam,posix_getpwuid, posix_getrlimit,  posix_getsid,posix_getuid,posix_isatty,  posix_kill,posix_mkfifo,posix_setegid,posix_seteuid,posix_setgid, posix_setpgid,posix_setsid,posix_setuid,posix_strerror,posix_times,posix_ttyname,posix_uname     #在386行 列出PHP可以禁用的函数，如果某些程序需要用到这个函数，可以删除，取消禁用
    ```  

    ```
    expose_php = Off              #在432行 禁止显示php版本的信息
    ```

    ```
    magic_quotes_gpc = On           #在745行 打开magic_quotes_gpc来防止SQL注入
    ```

    ```
    -------------------------------short_open_tag = ON  #在229行支持php短标签
    ```

    ```
    open_basedir = .:/tmp/           #在380行
    ```

    设置表示允许访问当前目录(即PHP脚本文件所在之目录)和/tmp/目录,可以防止php木马跨站,如果改了之后安装程序有问题，可以注销此行，或者直接写上程序的目录/data/web/:/tmp/

    ```
    :wq!                       #保存退出
    ```

    ```
    /etc/init.d/mysqld restart    # 重启Mysql
    ```

    ```
    /etc/init.d/httpd  restart    # 重启Apache
    ```

###配置防火墙，开启80、3306端口

- 防火墙添加80、3306  

    ```
    #vim /etc/sysconfig/iptables     #打开此表
    ```

    ```
    # Firewall configuration written by system-config-firewall
    ```

    ```
    # Manual customization of this file is not recommended.
    ```

    *filter

  ```
  :INPUT ACCEPT [0:0]
  :FORWARD ACCEPT [0:0]
  :OUTPUT ACCEPT [0:0]  
  -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT
  -A INPUT -p icmp -j ACCEPT
  -A INPUT -i lo -j ACCEPT  
  -A INPUT -m state --state NEW -m tcp -p tcp --dport 22 -j ACCEPT
  -A INPUT -m state --state NEW -m tcp -p tcp --dport 80 -j ACCEPT
  #添加  
  -A INPUT -m state --state NEW -m tcp -p tcp --dport 3306 -j ACCEPT  
  #添加  
  -A INPUT -j REJECT --reject-with icmp-host-prohibited
  -A FORWARD -j REJECT --reject-with icmp-host-prohibited
  COMMIT  
  /etc/init.d/iptables restart
  ```

- 关闭 SELINUX  
    ```
    # vi /etc/selinux/config
    ```

    把下面两项注释掉

  ```
  #SELINUX=enforcing   #注释掉
  #SELINUX=targeted    #注释掉
  SELINUX=disabled     #增加
  ```
  ```
  :wq!  # 保存退出
  ```

  ```
  # shutdown -r now
```

###[添加SWAP](https://www.digitalocean.com/community/articles/how-to-add-swap-on-centos-6)

- #####Check for Swap Space

    Before we proceed to set up a swap file, we need to check if any swap files have been enabled by looking at the summary of swap usage.

          swapon -s

    If nothing is returned, the summary is empty and no swap file exists.

- #####Check the File System

    After we know that we do not have a swap file enabled, we can check how much space we have on the server with the df command. The swap file will take 512MB— since we are only using up about 7% of the /dev/hda, we can proceed.

        df
        Filesystem           1K-blocks      Used Available Use% Mounted on
        /dev/hda              20642428   1347968  18245884   7% /

- #####Create and Enable the Swap File

    Now it’s time to create the swap file itself using the dd command :

        sudo dd if=/dev/zero of=/swapfile bs=1024 count=512k

    “of=/swapfile” designates the file’s name. In this case the name is swapfile.

    Subsequently we are going to prepare the swap file by creating a linux swap area:

        sudo mkswap /swapfile

    The results display:

        Setting up swapspace version 1, size = 536866 kB

    Finish up by activating the swap file:

        sudo swapon /swapfile

    You will then be able to see the new swap file when you view the swap summary.

          swapon -s
          Filename				Type		Size	Used	Priority
          /swapfile                               file		524280	0	-1

    This file will last on the server until the machine reboots. You can ensure that the swap is permanent by adding it to the fstab file.

    Open up the file:

          sudo nano /etc/fstab

    Paste in the following line:

          /swapfile          swap            swap    defaults        0 0

    阿里云默认是不让用户使用swap的。
    我们需要编辑/etc/rc.d/rc.local文件，将文件中的swapoff行注释或删掉。

        #swapoff -a

    To prevent the file from being world-readable, you should set up the correct permissions on the swap file:

        chown root:root /swapfile
        chmod 0600 /swapfile

    How To Configure Swappiness
    The operating system kernel can adjust how often it relies on swap through a configuration parameter known as swappiness. To find the current swappiness settings, type:

        cat /proc/sys/vm/swappiness
        60

    Swapiness can be a value from 0 to 100. Swappiness near 100 means that the operating system will swap often and usually, too soon. Although swap provides extra resources, RAM is much faster than swap space. Any time something is moved from RAM to swap, it slows down.

    A swappiness value of 0 means that the operating will only rely on swap when it absolutely needs to. We can adjust the swappiness with the sysctl command:

        sysctl vm.swappiness=10
        vm.swappiness=10

    If we check the system swappiness again, we can confirm that the setting was applied:

        cat /proc/sys/vm/swappiness
        10

    To make your VPS automatically apply this setting every time it boots up, you can add the setting to the /etc/sysctl.conf file:
    sudo nano /etc/sysctl.conf
    Search for the vm.swappiness setting.  Uncomment and change it as necessary.

        vm.swappiness=10
