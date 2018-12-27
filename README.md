"# git_learning" 

# 大概用来记录下怎么在vscode终端用git


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

## git忽略已经被提交的文件，解除track
忽略文件:
```
git rm --cached <PATH/fileName>
git commit -m'备注' <PATH/fileName>
git push
```
忽略文件夹所以文件：
```
git rm --cached -r <dirname>
git commit -m'备注' <dirname/file....>
git push
```
