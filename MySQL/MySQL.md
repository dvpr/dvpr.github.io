##MySQL

###多表删除

```
SELECT CONCAT("DROP TABLE ", GROUP_CONCAT(table_name), ";") FROM information_schema.tables WHERE table_schema = "DATABASE_NAME" AND table_name LIKE "PREFIX_TABLE_NAME%";
```

###创建用户

```
CREATE USER 'user_name'@'host' IDENTIFIED BY 'password';
```

###修改权限

```
grant all privileges on database_name.* to 'user_name'@'host' identified by 'user_password';
```


### MySQL REPLACE

```
UPDATE `table_name` SET `field_name` = REPLACE(`field_name`,'from_str','to_str');
```
