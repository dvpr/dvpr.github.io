## Rails

##### 创建scaffolding
##### generate scaffolding
```
rails generate scaffold your_scaffold_name
rails g scaffold your_scaffold_name # for short
```

##### 删除scaffolding
##### generate scaffolding
```
rails destroy scaffold your_scaffold_name
```

##### 创建migration
##### generate migration
```
rails generate migration your_migration_name
rails g migration your_migration_name # for short
# example
rails g migration add_group_id_to_users
rails g migration create_groups name:string level:integer # with fields
```