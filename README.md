# 大概用来记录下怎么在终端用git


## 下面是github自动推荐的初始化操作
```
echo "# git_learning" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/Icyfrog/git_learning.git
git push -u origin master
```
注意：要提前建好文件夹再执行上面操作，否则会让.git管理整个文件夹(当时是VsCode)，解决方案是，删除隐藏的.git文件夹

## 提交操作：
```
- git add . 将全部改动都track
- 这里用git add -A 也可以，只是git add. 不能track删除的文件操作
- 提交到本地库： git commit -m "commit messag any message"
- 将本地仓库和github下的仓库进行关联 git remote add origin https://github.com/chendi1991/git_test.git 
- 如果想要取消关联，可以使用下面的命令 git remote remove origin 
- 将本地的修改推送到远端的仓库中 git push -u origin master 

- 如果远端的版本比本地的高了，要先git pull
- 如果有branch分支情况 要git branch --set-upstream-to=origin/Newbranch
--------------------- 
```
## 分支操作
```
- 查看本地分支 git branch
- 查看远程分支 git branch -a
- 在本地新建一个分支： git branch newBranch
- 切换到你的新分支: git checkout newBranch
- 创建并切换到新分支： git checkout -b newBranch

- 将新分支发布在github上： git push origin newBranch（如果新建分支后，有更改的话，还要add，commit）
- 在新分支上工作，以后再提交之前需要设置upstream：git push --set-upstream origin newBranch

- 在本地删除一个分支： git branch -d newBranch
- 在github远程端删除一个分支：git push origin -d 分支名
- 从某分支下载 git clone xxx地址 -b newBranch

- 直接使用git pull和git push的设置,两种方式：意思是默认将本地的dev分支的推送到origin/dev
- git branch --set-upstream-to=origin/dev dev 
- git branch --set-upstream dev origin/dev
- git config --global push.default matching

```
## Fork了别人的repo之后的更新与提交代码
[check here ](https://blog.csdn.net/qq1332479771/article/details/56087333) 来看具体操作

## 删除操作：
```
git rm filename           Delete one file 
git rm -rf name           Delete one whole folder 
git add -A
git push
```
## 标签 tag
```
查看标签 git tag
创建标签 git tag -a v1.4 -m 'my version 1.4' 
删除标签 git tag -d v1.4
提交标签 git push origin v1.5
```
## git忽略已经被提交的文件，解除track
忽略文件:
```
git rm --cached <PATH/fileName>
git commit -m'备注' <PATH/fileName>         // 这句commit不知道有啥用
git push
```
忽略文件夹所以文件：
```
git rm --cached -r <dirname>
git commit -m'备注' <dirname/file....>       // 这句commit不知道有啥用
git push
```
