git如何把master上的代码，合并到自己的分支

1.切换到主分支 （master）

> git checkout master

2.拉去远程仓库的代码

> git pull

3.在切换到自己的分支

> git checkout 分支名称

4.把主分支的代码merge合并到自己的分支上面

> git merge master

5.使用上传命令push

> git push origin 自己的分支

## 相反

把自己的代码 **push** 合并进主分支

> git checkout master

合并

> git merge 自己的分支

这样就完成了，从主分支上的代码拉去到自己的分支的具体流程
