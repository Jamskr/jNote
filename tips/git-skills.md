# git 常用技巧

## 1. 配置用户名和邮箱
```
git config --global user.name "Jam"
git config --global user.email "jam@lircs.com"
```

## 2. 添加多个远程仓库
```
git remote add mirror git@xxx.git

git pull mirror
git push mirror master

git pull origin
git push origin master
```

## 3. 查看单个文件历史和提交
```
git log fileName // git log -- fileName
git log -p fileName
git log --pretty=oneline fileName
gitk --follow fileName
```