## Laravel

### 常用命令行

```
php artisan migrate //执行数据迁移
php artisan make:migration migrate_name --create="table_name" //创建表
php artisan make:migration migrate_name --table="table_name" //更新表

php artisan make:model model_name //创建模型
php artisan make:controller controller_name //创建控制器
```

##### Laradock 修改PHP全局配置
##### Laradock configures the PHP development environment
```
vi laradock/php-fpm/laravel.ini # custom ini file will cover default settings.
docker-compose up -d php-fpm –force-recreate # rebuild container and start.
```
