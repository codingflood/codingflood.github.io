---
title: 本地修改上传到github库

author: Algar

date: 2018-11-02

---
一、我们在github上创建仓库，然后git clone到本地，比如我的,codingflood是我的用户名，codingflood.github.io就是我的仓库名：

```
git clone https://github.com/codingflood/codingflood.github.io.git
```

二、clone到本地后，我们先cd进入仓库文件夹（codingflood.github.io），然后git init初始化，告诉git可以管理这个仓库。
```
git init
```
三、添加文件到版本库，其实这个时候是把文件添加到暂时储存区域，还未上传到github上面。

1.添加指定文件方式
```
git add /path/<filename>
```
2.添加所有文件方式（git add 后面空格加一个小点）
```
git add .
```
四、文件提交到github仓库前，先提交本次变动的说明注释
```
git commit -m '注释内容'
```
五、本地仓库与github仓库的关联
```
git remote add origin <repo在上github的远程地址>
```
例如，我的
```
git remote add origin https:github.com/codingflood/codingflood.github.io.git
```
六、本地仓库与github上的仓库同步合并
```
git pull --rebase origin master
```
七、把本地内容上传到github上面，输入以下命令后，再输入你的用户名和密码，其中用户名是显示的，密码是不显示的
```
git push -u origin master
```
上传成功会显示上传成功的详细信息，不成功也有不成功的信息，以后本地内容有修改更新要同步到github上面的话，按第二到第四，第六到第七步骤操作即可。
最后，可以进行状态查询
```
git status
```












