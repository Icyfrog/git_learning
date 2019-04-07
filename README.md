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
先改了文件后，如果不想一个一个输入git add 文件名，
用 git add . 将全部改动都track
这里用git add -A 也可以，只是git add. 不能track删除的文件操作
git commit操作的是本地库，git push操作的是远程库。
git commit是将本地修改过的文件提交到本地库中。
git push是将本地库中的最新信息发送给远程库。
```
## 分支操作
```
查看本地分支 git branch
查看远程分支 git branch -a
删除本地分支 git branch -d 分支名
删除远程分支 git push origin -d 分支名
本地创建并切换到分支 git checkout -b 分支名
本地创建分支 git branch 分支名  目前在那个分支，提交的时候就会在哪个分支上
从某分支下载 git clone xxx地址 -b 分支名

```
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
