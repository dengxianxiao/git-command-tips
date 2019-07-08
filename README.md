# git-command-tips

记录一下平时经常使用的命令，遇到的问题

## 提交本地分支到远程

```js
git push origin branch-name
```

## 清除远程已删除，但是在本地查看远程分支时还存在的分支

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

## 删除远程分支

```js
git push origin --delete <branchName>
```

## 本地分支与远程分支关联

遇到的报错

fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

git push --set-upstream origin dev

```js
git push --set-upstream origin dev
// 或者
git branch -u origin dev
```

## 删除本地分支和远程分支

```js
// 查看当前分支
git branch -a

// 删除本地分支
git branch -d <branchName>

// 删除远程分支
git push origin --delete <branchName>
```
