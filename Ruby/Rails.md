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

##### Migration回滚
##### Migration rollback
```
rake db:rollback # rollback step 1
rake db:rollback STEP=n # rollback step n
rake db:migrate:down VERSION=version_number # rollback to version_number
```

##### 创建或更新一条数据
##### Update or create a record in Active Record.
```
ModelName.find_or_initialize_by(feild1: feild1_of_find_by, feild2: feild2_of_find_by).update_attributes!(feild_need_update: feild_need_update_value)
```