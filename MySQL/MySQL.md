##Mysql

###多表删除

```
SELECT CONCAT("DROP TABLE ", GROUP_CONCAT(table_name), ";") FROM information_schema.tables WHERE table_schema = "DATABASE_NAME" AND table_name LIKE "PREFIX_TABLE_NAME%";
```

###创建用户

```
CREATE USER 'username'@'host' IDENTIFIED BY 'password';
```

###修改权限

```
grant all privileges on joomla.* to joomla@localhost identified by 'joomla!Q@W#E$R';
```
