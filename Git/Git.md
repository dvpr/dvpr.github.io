## Git

<br /><br />

##### Conventional Commits

```
feat：新功能（feature）
fix：修补bug
docs：文档（documentation）
style： 格式（不影响代码运行的变动）
refactor：重构（即不是新增功能，也不是修改bug的代码变动）
test：增加测试
chore：构建过程或辅助工具的变动
```

<br /><br />

##### 储存登录信息
##### Store password

```
git config credential.helper store
```

<br /><br />

##### 删除本地Add文件或文件夹
##### Delete local add file/folder

```
git rm --cached path_to_your_file
git rm -f --cached path_to_your_folder
```

<br /><br />

##### 彻底清理Git库中某个文件
##### Clean file and history
##### this exceeds GitHub's file size limit of 100 MB

```
git filter-branch -f --index-filter 'git rm --cached --ignore-unmatch path_to_your_file'
```

<br /><br />

##### Git branch
##### Git 分支

```
$ git branch # 查看本地分支
$ git branch -r # 查看远程分支
$ git branch -a # 查看所有分支
$ git branch -vv # 查看本地分支及追踪的分支

$ git branch 分支名 # 创建本地分支
$ git checkout -b 分支名 origin/远程分支名 

$ git checkout 分支名 # 切换本地分支
$ git checkout -b 分支名 # 切换远程分支

$ git branch -d 分支名 # 删除本地分支
$ git push origin --delete 分支名 # 删除远程分支
```