# git-command-tips

记录一下平时经常使用的命令，遇到的问题

## 1. 提交本地分支到远程

```js
$ git push origin branch-name
```

## 2.清除远程已删除，但是在本地查看远程分支时还存在的分支

```js
$ git branch -a
// 远程dev分支已经被合并删除了，但是本地查看还存在
* dev
  master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master

$ git pull -p
// 远程分支已经没有了dev，只有本地的dev分支，可以git branch -d dev 删除本地分支(不建议删除，留着本地备份比较好)
* dev
  master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
```