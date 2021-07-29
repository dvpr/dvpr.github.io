## Symfony

### 安装记录

Preparing project...

✔ Symfony 2.3.25 was successfully installed. Now you can:

```
* Change your current directory to /var/www/html/labs/vduor

* Configure your application in app/config/parameters.yml file.

* Run your application:
    1. Execute the php app/console server:run command.
    2. Browse to the http://localhost:8000 URL.

* Read the documentation at http://symfony.com/doc
```

Start...

### 常用命令行

```
php app/console generate:bundle --namespace=Ens/JobeetBundle --format=yml                               //创建程序
php app/console doctrine:generate:entities EnsJobeetBundle                                              //生成数据模型
php app/console doctrine:schema:update --force                                                          //更新数据结构
php app/console assets:install                                                                          //更新媒体
php app/console cache:clear --env=prod                                                                  //清理缓存
php app/console cache:clear --env=dev                                                                   //清理缓存
php app/console doctrine:generate:crud --entity=EnsJobeetBundle:Job --route-prefix=ens_job --with-write --format=yml
```

### 添加excel bundle

```
php ../composer.phar update liuggio/excelbundle
```

The command was not able to configure everything automatically. You must do the following changes manually.
