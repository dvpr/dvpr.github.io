## MySQL

### 多表删除

```
SELECT CONCAT("DROP TABLE ", GROUP_CONCAT(table_name), ";") FROM information_schema.tables WHERE table_schema = "DATABASE_NAME" AND table_name LIKE "PREFIX_TABLE_NAME%";
```

### 创建用户

```
CREATE USER 'user_name'@'host' IDENTIFIED BY 'password';
```

### 修改权限

```
grant all privileges on database_name.* to 'user_name'@'host' identified by 'user_password';
```


### MySQL REPLACE

```
UPDATE `table_name` SET `field_name` = REPLACE(`field_name`,'from_str','to_str');
```

### MySQL 权限备忘

| Privilege | Grant Table Column | Context |
| :----- | :----- | :----- |
| ALL [PRIVILEGES] | Synonym for “all privileges” | Server administration |
| ALTER | Alter_priv | Tables |
| ALTER ROUTINE | Alter_routine_priv | Stored routines |
| CREATE | Create_priv | Databases, tables, or indexes |
| CREATE ROUTINE | Create_routine_priv | Stored routines |
| CREATE TABLESPACE | Create_tablespace_priv | Server administration |
| CREATE TEMPORARY TABLES | Create_tmp_table_priv | Tables |
| CREATE USER | Create_user_priv | Server administration |
| CREATE VIEW | Create_view_priv | Views |
| DELETE | Delete_priv | Tables |
| DROP | Drop_priv | Databases, tables, or views |
| EVENT | Event_priv | Databases |
| EXECUTE | Execute_priv | Stored routines |
| FILE | File_priv | File access on server host |
| GRANT OPTION | Grant_priv | Databases, tables, or stored routines |
| INDEX | Index_priv | Tables |
| INSERT | Insert_priv | Tables or columns |
| LOCK TABLES | Lock_tables_priv | Databases |
| PROCESS | Process_priv | Server administration |
| PROXY | See proxies_priv table | Server administration |
| REFERENCES | References_priv | Databases or tables |
| RELOAD | Reload_priv | Server administration |
| REPLICATION CLIENT | Repl_client_priv | Server administration |
| REPLICATION SLAVE | Repl_slave_priv | Server administration |
| SELECT | Select_priv | Tables or columns |
| SHOW DATABASES | Show_db_priv | Server administration |
| SHOW VIEW | Show_view_priv | Views |
| SHUTDOWN | Shutdown_priv | Server administration |
| SUPER | Super_priv | Server administration |
| TRIGGER | Trigger_priv | Tables |
| UPDATE | Update_priv | Tables or columns |
| USAGE | Synonym for “no privileges” | Server administration |
