# GIT

### 如何写git commit message

How to Write a Git Commit Message: https://chris.beams.io/posts/git-commit/

## 使用说明

### 配置用户及邮箱

```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

### 配置文本编辑器

```
git config --global core.editor vim
```

### 配置差异分析工具

```
git config --global merge.tool vimdiff
```

### 差异分析工具合集

kdiff3，tkdiff，meld，xxdiff，emerge，vimdiff，gvimdiff，ecmerge

### 查看配置信息

```
git config --list
```

### clone的时候使用自己命名的目录

```
git clone git://github.com/schacon/grit.git mygrit
```

git config remote.origin.push HEAD:refs/for/branch1

git commit --amend

### 保存本地临时修改，合入master

```
git stash save -- "add the case"
git stash list
git checkout <other branch>
git stash pop
#如果存在冲突的话，需要解决冲突
```

### push 到 gerrit

```
git push origin HEAD:refs/for/branch1
```

git log
 http://eclipseupd.china.nsn-net.net/svnlog

git apply --whitespace=fix your.patch 

### 查看指定作者的提交记录

```
git log --author=xiujuan --oneline
```

### 取消最近的一次操作

```
git reset --soft HEAD~1
```

### 取消对文件的git add操作

```
git reset HEAD file
```

### 查看远程仓库地址

```
git remote -v
```

### 代码文件格式

​        格式化是许多开发人员在协作时，特别是在跨平台情况下，遇到的令人头疼的细小问题。 由于编辑器的不同或者Windows程序员在跨平台项目中的文件行尾加入了回车换行符， 一些细微的空格变化会不经意地进入大家合作的工作或提交的补丁中。不用怕，Git的一些配置选项会帮助你解决这些问题。
core.autocrlf
​        假如你正在Windows上写程序，又或者你正在和其他人合作，他们在Windows上编程，而你却在其他系统上，在这些情况下，你可能会遇到行尾 结束符问题。 这是因为Windows使用回车和换行两个字符来结束一行，而Mac和Linux只使用换行一个字符。 虽然这是小问题，但它会极大地扰乱跨平台协作。
Git可以在你提交时自动地把行结束符CRLF转换成LF，而在签出代码时把LF转换成CRLF。用core.autocrlf来打开此项功能， 如果是在Windows系统上，把它设置成true，这样当签出代码时，LF会被转换成CRLF：

```
$ git config --global core.autocrlf true
```

​        Linux或Mac系统使用LF作为行结束符，因此你不想Git在签出文件时进行自动的转换；当一个以CRLF为行结束符的文件不小心被引入时你肯定想进行修正， 把core.autocrlf设置成input来告诉Git在提交时把CRLF转换成LF，签出时不转换：

```
$ git config --global core.autocrlf input
```

​        这样会在Windows系统上的签出文件中保留CRLF，会在Mac和Linux系统上，包括仓库中保留LF。
如果你是Windows程序员，且正在开发仅运行在Windows上的项目，可以设置false取消此功能，把回车符记录在库中：

```
$ git config --global core.autocrlf false
```

### 查看权限    

```
git ls-tree HEAD
```

### 修改权限

```
git update-index --chmod=+x script.sh
```


git branch -d the_local_branch

### gerrit rebase

```
git pull --rebase origin rcp2.0
git merge --no-ff remotes/origin/rcp2.0
```

### 回退--amend

```
git reset --soft @{1}
git commit -C @{1}
```

### 用squash合并commit 

```
git rebase -i master
git push --force origin <my branch>
```

### 配置git merge的工具

```
git config merge.tool vimdiffgit config merge.conflictstyle diff3git config mergetool.prompt false
```



```
git mergetool
git commit --author="John Doe "
```



### 查找git文件归属

```
git blame Dockerfile-stub
```

