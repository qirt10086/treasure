# git使用

## rebase变基

### 场景一

如果远程分支有更新，本地分支落后于远程

#### 解决方案

1. `git pull --rebase <origin> <main>`
   - 拉取远程分支的最新更新，并使用rebase方式合并到本地分支
   - <origin>:远程仓库名称
   - <main>:远程分支名称
  
2. `git push <origin> <main>`
   - 将本地分支推送到远程分支
   - <origin>:远程仓库名称
   - <main>:本地分支的名称

### 场景二

开发分支，和主分支都分别提交到github远端，想要合并分支

### 解决方案

1. `git checkout <dev>`
   - 切换到开发分支
2. `git rebase <main>`
   - 将开发分支与主分支进行变基，将开发分支的修改合并到主分支
3. `git rebase --continue`(发生冲突可能需要)
   - 继续执行rebase操作


## 手动提交代码

1. `git add .`
   - 添加所有修改的文件到暂存区

2. `git commit -m "<xxx>"`
   - 提交修改到本地仓库
   - <xxx>:提交信息

3. `git push`
   - 将本地仓库推送到远程仓库
