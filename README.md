- [ 推荐教程](#head1)
- [第一章：Git 基础 (13 讲)](#head2)
	- [01 | 课程综述](#head3)
	- [02 | 安装 Git](#head4)
	- [03 | 使用 Git 之前需要做的最小配置](#head5)
	- [04 | 创建第一个仓库并配置 local 用户信息](#head6)
	- [05 | 通过几次 commit 来认识工作区和暂存区](#head7)
	- [06 | 给文件重命名的简便方法](#head8)
	- [07 | 通过 git log 查看版本演变历史](#head9)
	- [08 | gitk：通过图形界面工具来查看版本历史](#head10)
	- [09 | 探密. git 目录](#head11)
	- [10 | commit、tree 和 blob 三个对象之间的关系](#head12)
	- [11 | 小练习：数一数 tree 的个数](#head13)
	- [12 | 分离头指针情况下的注意事项](#head14)
	- [13 | 进一步理解 HEAD 和 branch](#head15)
- [第二章：独自使用 Git 时的常见场景 (16 讲)](#head16)
	- [14 | 怎么删除不需要的分支？](#head17)
	- [15 | 怎么修改最新 commit 的 message？](#head18)
	- [16 | 怎么修改老旧 commit 的 message？](#head19)
	- [17 | 怎样把连续的多个 commit 整理成 1 个？](#head20)
	- [18 | 怎样把间隔的几个 commit 整理成 1 个？](#head21)
	- [19 | 怎么比较暂存区和 HEAD 所含文件的差异？](#head22)
	- [20 | 怎么比较工作区和暂存区所含文件的差异？](#head23)
	- [21 | 如何让暂存区恢复成和 HEAD 的一样？](#head24)
	- [22 | 如何让工作区的文件恢复为和暂存区一样？](#head25)
	- [23 | 怎样取消暂存区部分文件的更改？](#head26)
	- [24 | 消除最近的几次提交](#head27)
	- [25 | 看看不同提交的指定文件的差异](#head28)
	- [26 | 正确删除文件的方法](#head29)
	- [27 | 开发中临时加塞了紧急任务怎么处理？](#head30)
	- [28 | 如何指定不需要 Git 管理的文件？](#head31)
	- [29 | 如何将 Git 仓库备份到本地？](#head32)
- [第三章：Git 与 GitHub 的简单同步 (4 讲)](#head33)
	- [30 | 注册一个 GitHub 账号](#head34)
	- [31 | 配置公私钥](#head35)
	- [32 | 在 GitHub 上创建个人仓库](#head36)
	- [33 | 把本地仓库同步到 GitHub](#head37)
- [第四章：Git 多人单分支集成协作时的常见场景 (5 讲)](#head38)
	- [34 | 不同人修改了不同文件如何处理？](#head39)
	- [35 | 不同人修改了同文件的不同区域如何处理？](#head40)
	- [36 | 不同人修改了同文件的同一区域如何处理？](#head41)
	- [37 | 同时变更了文件名和文件内容如何处理？](#head42)
- [ 一个人改了文件名，一个人改了文件内容，还是可以自动处理的。](#head43)
- [38 | 把同一文件改成了不同的文件名如何处理？](#head44)
- [ 人为判断需保留哪一个文件。](#head45)
- [第五章：Git 集成使用禁忌 (2 讲)](#head46)
	- [39 | 禁止向集成分支执行 push -f 操作](#head47)
	- [40 | 禁止向集成分支执行变更历史的操作](#head48)
- [第六章：初识 GitHub (6 讲)](#head49)
	- [41 | GitHub 为什么会火？](#head50)
	- [42 | GitHub 都有哪些核心功能？](#head51)
	- [43 | 怎么快速淘到感兴趣的开源项目?](#head52)
	- [44 | 怎样在 GitHub 上搭建个人博客](#head53)
	- [45 | 开源项目怎么保证代码质量？](#head54)
	- [46 | 为何需要组织类型的仓库？](#head55)
- [第七章：使用 GitHub 进行团队协作 (10 讲)](#head56)
	- [47 | 创建团队的项目](#head57)
	- [48 | 怎样选择适合自己团队的工作流？](#head58)
	- [49 | 如何挑选合适的分支集成策略？](#head59)
	- [50 | 启用 issue 跟踪需求和任务](#head60)
	- [51 | 如何用 project 管理 issue？](#head61)
	- [52 | 项目内部怎么实施 code review？](#head62)
	- [53 | 团队协作时如何做多分支的集成？](#head63)
	- [54 | 怎样保证集成的质量？](#head64)
	- [55 | 怎样把产品包发布到 GitHub 上？](#head65)
	- [56 | 怎么给项目增加详细的指导文档？](#head66)
- [第八章：GitLab 实践 (6 讲)](#head67)
	- [57 | 国内互联网企业为什么喜欢 GitLab？](#head68)
	- [58 | GitLab 有哪些核心的功能？](#head69)
	- [59 | GitLab 上怎么做项目管理？](#head70)
	- [60 | GitLab 上怎么做 code review？](#head71)
	- [61 | GitLab 上怎么保证集成的质量？](#head72)
	- [62 | 怎么把应用部署到 AWS 上？](#head73)



## <span id="head1"> 推荐教程</span>

学习git系列教程 ：[https://github.com/xirong/my-git](https://github.com/xirong/my-git)
实践练习 进行对Git学习 : [https://learngitbranching.js.org/?locale=zh_CN](https://learngitbranching.js.org/?locale=zh_CN)



# <span id="head2">第一章：Git 基础 (13 讲)</span>
### <span id="head3">01 | 课程综述</span>

Git 官网：
https://git-[scm](https://so.csdn.net/so/search?q=scm&spm=1001.2101.3001.7020).com

GitHub：
[https://github.com](https://github.com)

GitLab：
[https://about.gitlab.com](https://about.gitlab.com)

### <span id="head4">02 | 安装 Git</span>

[https://git-scm.com/book/zh/v2](https://git-scm.com/book/zh/v2)

### <span id="head5">03 | 使用 Git 之前需要做的最小配置</span>

```
# 本节知识点

## 添加配置

git config [--local | --global | --system] user.name 'Your name'
git config [--local | --global | --system] user.email 'Your email'

## 查看配置

git config --list [--local | --global | --system]

## 区别

local：区域为本仓库
global: 当前用户的所有仓库
system: 本系统的所有用户
```

### <span id="head6">04 | 创建第一个仓库并配置 local 用户信息</span>

1）第一种理解
本地有个项目代码写了一段时间了，但还没有用 git 管理起来，现在想用 git 在本地帮着记录变更的版本。  
2）第二种理解  
很早之前本地生成了一个 git 的仓库，开发了一段时间，想把这个 git 仓库提交到公司 git 服务器新建的 project 中。  

对于第一种理解：
1.cd existing_folder （本地进入到项目文件夹内）  
2.git init （执行 init 命令，会创建出 .git 目录）  
3.git add . （把项目文件加入到 git 的暂存区）  
4.git commit -m “Initial commit” （创建第一个 git 的 commit ）  
3、4步可以简单替代为   
git commit -am "Initial commit"  
对于第二种理解：  
cd existing_repo  
git remote add origin git@your_git_server:your_group/your_project.git  
git push -u origin --all  
git push -u origin --tags  

### <span id="head7">05 | 通过几次 commit 来认识工作区和暂存区</span>  

git add -u：将文件的修改、文件的删除，添加到暂存区。  
git add .：将文件的修改，文件的新建，添加到暂存区。  
git add -A：将文件的修改，文件的删除，文件的新建，添加到暂存区。   
工作中一般是用到 git add . 或者 git add -A, 今天学习更进一步解了 git add -u 以及他们之间的区别，谢谢苏玲老师讲的很详细 git add -A相对于git add -u命令的优点 ： 可以提交所有被删除、被替换、被修改和新增的文件到数据暂存区，而git add -u 只能操作跟踪过的文件 git add -A 等同于git add -all  

### <span id="head8">06 | 给文件重命名的简便方法</span>  

mv readme readme.md 删除文件readme 创建新文件readme.md   
git add readme.md 添加到暂存区  
 git rm readme 将原来的文件删除掉  
 这三步可以直接变成一步 git mv readme readme.md 将readme重新命名成readme.md  

### <span id="head9">07 | 通过 git log 查看版本演变历史</span>  

本节的一些演示命令总结
• git log --all 查看所有分支的历史
• git log --all --graph 查看图形化的 log 地址
• git log --oneline 查看单行的简洁历史。
• git log --oneline -n4 查看最近的四条简洁历史。
• git log --oneline --all -n4 --graph 查看所有分支最近 4 条单行的图形化历史。
• git help --web log 跳转到 git log 的帮助文档网页
[git log 的使用](https://www.jianshu.com/p/0805b5d5d893)

![image.png](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855672.png)


### <span id="head10">08 | gitk：通过图形界面工具来查看版本历史</span>

gitk
![image.png](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855677.png)

### <span id="head11">09 | 探密. git 目录</span>
[Git目录为什么这么大](https://links.jianshu.com/go?to=https%3A%2F%2Fcloud.tencent.com%2Fdeveloper%2Farticle%2F1870732)
cat HEAD 查看 HEAD 文件的内容  
git cat-file 命令 显示版本库对象的内容、类型及大小信息。  
git cat-file -t b44dd71d62a5a8ed3 显示版本库对象的类型  
git cat-file -s b44dd71d62a5a8ed3 显示版本库对象的大小  
git cat-file -p b44dd71d62a5a8ed3 显示版本库对象的内容(查看commit下的内容)  
![image.png](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855673.png)  



HEAD：指向当前的工作路径  
config：存放本地仓库（local）相关的配置信息。  
refs/heads: 存放分支  
refs/tags: 存放 tag，又叫里程牌 （当这次 commit 是具有里程碑意义的 比如项目 1.0 的时候 就可以打 tag）  
objects：存放对象 .git/objects/ 文件夹中的子文件夹都是以哈希值的前两位字符命名 每个 object 由 40 位字符组成，前两位字符用来当文件夹，后 38 位做文件。  
[HEAD、master 与 branch](https://www.jianshu.com/p/4219b6f62ce3)  
### <span id="head12">10 | commit、tree 和 blob 三个对象之间的关系</span>  
[BLOB、Commit和Tree组件](https://www.jianshu.com/p/8659c9ae00cb)

![image.png](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855675.png)
如果是文件夹上传，那么体现在git的commit的话，就是以tree的模式来提交。  



git 有 3 种对象：commit、tree、blob。每次的提交，都是一个 commit，一个 commit 又是包含了一棵 tree，每个 tree 里面又是包含了多棵 tree 和 blob，而文件的的最终形式是 blob。对于 blob，git 会认为文件内容相同，就使用同一个 blob，这样就极大的避免了频繁的提交时，git 的存储空间的急剧上升。  

每一次 commit 都对应一个 tree，那这个 tree 是包裹在最外层的一个 tree，使用 git cat-file -p 命令的时候查看 tree 内部的内容，这里的每一个文件夹都可以看成一个 tree，而在这些文件夹中的具体文件内容两两不相等文件都是一个 blob，内容相同的文件统一为一个 blob。  


### <span id="head13">11 | 小练习：数一数 tree 的个数</span>

略

### <span id="head14">12 | 分离头指针情况下的注意事项</span>
[Git操作 — 67.分离头指针状态](https://www.jianshu.com/p/de099617455b)
那分离头指针在企业或日常使用中, 到底有哪些具体的适用地点呢?

如果临时想基于某个 commit 做变更，试试新方案是否可行，就可以采用分离头指针的方式。测试后发现新方案不成熟，直接 reset 回其他分支即可。省却了建、删分支的麻烦了。

git checkout commitId：会出现分离头指针的情况，这种情况下比较危险，因为这个时候你提交的代码没有和分支对应起来，当切换到其他分支的时候 (比如 master 分支)，容易丢失代码；但是分离头指针也有它的应用场景，就是在自己做尝试或者测试的时候可以分离头指针，当尝试完毕没有用的时候可以随时丢弃，但是如果觉得尝试有用，那么可以新建一个分支，使用 git branch < 新分支的名称 > commitId


### <span id="head15">13 | 进一步理解 HEAD 和 branch</span>

- HEAD可以脱离branch而存在，但一定会最终指向某一个具体的commit。
- 切换branch时HEAD会自动切换至该branch最新一次的commit上。
- 分离HEAD的场景下切换至branch会使得在分离HEAD场景中做的修改丢失，所以一般情况下慎用分离HEAD。
- 由于HEAD一定会指向一个具体的commit，所以执行某些git命令是可以把HEAD当作是具体commit的别名。例如：
```java
// 比较最新一次和上上次提交的差异。
git diff HEAD HEAD^^ // 在具体分支上HEAD就是指最新一次的提交
// 等价于
git diff HEAD HEAD~2
```
# <span id="head16">第二章：独自使用 Git 时的常见场景 (16 讲)</span>
**注意本章节提到的大部分命令都是独自使用Git的场景**
### <span id="head17">14 | 怎么删除不需要的分支？</span>

_**创建开发(develop)分支 git branch develop**_
_**切换develop分支 git checkout develop**_

git branch -d branch_name: 使用 - d 在删除前 Git 会判断在该分支上开发的功能是否被 merge 的其它分支。如果没有，不能删除。如果 merge 到其它分支，但之后又在其上做了开发，使用 - d 还是不能删除。-D 会强制删除。  

### <span id="head18">15 | 怎么修改最新 commit 的 message？</span>
git commit --amend 对最新一次提交做 commit 修改  

### <span id="head19">16 | 怎么修改老旧 commit 的 message？</span>
修改历史的 Commit message，通常用在还没有提交到集成分支之前：
`git rebase -i father_commit_id`
交互界面里的命令选 reword

### <span id="head20">17 | 怎样把连续的多个 commit 整理成 1 个？</span>

把连续的多个 Commit 合并为 1 个：
`git rebase -i father_commit_id`  
交互界面里的命令选 squash，并输入新的 commit message  

### <span id="head21">18 | 怎样把间隔的几个 commit 整理成 1 个？</span>

修改最新的：git commit --amend  
修改老旧的：git rebase --xxxxxxx pick 改为 r reword  
合并连续的：git rebase --xxxxxxx(父 commit id) 保留较老的 pick，其他要合并的使用 s squash  
合并不连续的：git rebase --xxxxxxx(父 commit id) 保留较老的 pick, 其他要合并的移动到第二行，使用 s。如果没有父 commit id。用 git rebase -i --root，或者手动加上。  
[Git 合并多个 commit，保持历史简洁](https://links.jianshu.com/go?to=https%3A%2F%2Fcloud.tencent.com%2Fdeveloper%2Farticle%2F1690638)

### <span id="head22">19 | 怎么比较暂存区和 HEAD 所含文件的差异？</span>

vi index.html 修改 index.html 的内容  
git add index.html 将修改的文件添加到暂存区  
git status 显示在哪个暂存区 有没有文件改变将要提交  
git diff --cached 查看文件改变情况 看变更的文件有没有问题  
git commit -m’Add the frist command with config’ 做提交操作  

### <span id="head23">20 | 怎么比较工作区和暂存区所含文件的差异？</span>

假定：HEAD、缓存区、工作区中的 readme.md 文件内容均不相同。  
git diff HEAD – readme.md # 工作区 <===> HEAD  
git diff – readme.md # 工作区 < => 缓存区  
git diff --cached – readme.md # 缓存区 <=> HEAD  

### <span id="head24">21 | 如何让暂存区恢复成和 HEAD 的一样？</span>

git reset 有三个参数  
–soft 这个只是把 HEAD 指向的 commit 恢复到你指定的 commit，暂存区 工作区不变  
–hard 这个是 把 HEAD， 暂存区， 工作区 都修改为 你指定的 commit 的时候的文件状态  
–mixed 这个是不加时候的默认参数，把 HEAD，暂存区 修改为 你指定的 commit 的时候的文件状态，工作区保持不变  

### <span id="head25">22 | 如何让工作区的文件恢复为和暂存区一样？</span>

舍弃 html 文件的修改  
git checkout – index.html（有个空格）  
或新版本  
git restore index.html  

### <span id="head26">23 | 怎样取消暂存区部分文件的更改？</span>

git reset HEAD ，是让暂存区恢复为 HEAD 所指向的节点，使用了该命令后，工作区修改的内容会被保留（保险），如果本地的修改需要丢弃掉，那么可使用–hard  

### <span id="head27">24 | 消除最近的几次提交</span>

修改了工作区，恢复：git checkout  

add 后，想撤销： git reset HEAD

commit 后，想撤销： git reset–hard hash 值  

### <span id="head28">25 | 看看不同提交的指定文件的差异</span>

git diff commit-id1 commit-id2 path-to-filename  

对不同的分支进行差异化的比较使用 git diff commit_id commit_id – index.html  

### <span id="head29">26 | 正确删除文件的方法</span>

本课使用【rm 】先删除工作区的文件后，再使用命令【git add < filename>】提交到暂存区中，效果和使用【rm < filename>】再使用【git rm < filename>】一样。只是【git rm < filename>】可以省略本地工作区【rm < filename>】这个命令的操作步骤。  
总结：直接在工作区和暂存区中删除某个将来不需要提交到 commit 的文件时，使用命令【git rm 】即可。  

### <span id="head30">27 | 开发中临时加塞了紧急任务怎么处理？</span>

git stash 将手头正在修改的东西先存起来放到一边去处理紧急任务  

git stash apply  
第一个作用将之前 git stash 存放的内容弹出来 把他的东西放到工作区去  
第二个使用 git stash list 查看链表里的内容还在可以进行反复使用  

git stash pop 和 stash 的区别 pop 中 list 不保留 apply 保留  

### <span id="head31">28 | 如何指定不需要 Git 管理的文件？</span>

.gitinore 对其中的内容进行配置，可以设置 git 不用管理的文件或者文件夹  
doc 是不管理这个文件夹和文件  
doc / 不管文件夹管文件  

### <span id="head32">29 | 如何将 Git 仓库备份到本地？</span>

1）找个目录执行 clone 。
2）用 init 建个 git 仓库，然后从备份数据库添加 remote，再 push 到新建仓库；  
3）或者用 init 建个 git 仓库，然后在新仓库添加 remote，再把备份数据库 fetch/pull 到新仓库。  

```
# 本地模拟推送，git备份

## 远程库

git clone --bare file:///XXXX/.git  remoteRepoName.git  

bare不包含工作区，作为远端，以后备份方便一点  

这样的话，已经备份了  

## 本地仓库

跟远程库建立关联  

git remote add remoteRepoName file:///XXXX/remoteRepoName.git  

本地发送一些改动，比如新增分支develop  

推送分支变动到远程  

git push --set-upstream remoteRepoName develop  

再到远程库下面查看就会发现远程也有develop分支了  
```

# <span id="head33">第三章：Git 与 GitHub 的简单同步 (4 讲)</span>

### <span id="head34">30 | 注册一个 GitHub 账号</span>

略

### <span id="head35">31 | 配置公私钥</span>

首次生成密钥时还需要执行一下命令
ssh-add ~/.ssh/id_rsa

github 网站更新后，配置 SSH keys 的入口在：右上角头像 --> Settings --> 左侧导航栏的 SSH and GPG keys

### <span id="head36">32 | 在 GitHub 上创建个人仓库</span>

略

本地分支往远端分支做 push，如果远端分支不是本地分支的祖先，那它俩就不是 fast forward 了。反之，它俩就是 fast forward 的关系。

### <span id="head37">33 | 把本地仓库同步到 GitHub</span>

个人笔记总结
git remote -v 查看远程版本库信息  
git remote add github  添加 github 远程版本库  
git fetch github 拉取远程版本库  
git merge -h 查看合并帮助信息  
git merge --allow-unrelated-histories github/master 合并 github 上的 master 分支（两分支不是父子关系，所以合并需要添加 --allow-unrelated-histories）  
git push github 推送同步到 github 仓库  

# <span id="head38">第四章：Git 多人单分支集成协作时的常见场景 (5 讲)</span>

### <span id="head39">34 | 不同人修改了不同文件如何处理？</span>

每次 push 本地代码之前 pull 一下远端代码，然后在 push，就没有问题了。  

老师你好，我有个问题哈，clone 命令 git clone [git@github.com](mailto:git@github.com):git2019/git_learning.git 既然已经把远程仓库所有内容都克隆到本地了，为什么还需要 git checkout -b feature/add_git_commands origin/feature/add_git_command 命令基于远程分支在本地建立分支，不是从远程 clone 下来了嘛，为什么还要新建，难道 clone 命令不能克隆分支嘛  
作者回复: 我们在本地无法直接在 clone 下来的远程分支上做变更的，只能基于远程分支建本地分支后，才能创建 commit  

### <span id="head40">35 | 不同人修改了同文件的不同区域如何处理？</span>

git pull 相对于两步 git fetch+merge 在什么场景下有问题？谢谢。  
作者回复: 比如，团队有 3 个人共同维护一个特性分支，你们在本地直接在该分支上做开发。你的本地功能还没有开发完，还不想和远端的特性分支做集成，只是想看看和远端分支的差异，此时，就可以先执行 fetch，而不用 pull 。  

### <span id="head41">36 | 不同人修改了同文件的同一区域如何处理？</span>

git 使用原则
1：push 前一定先 pull  
2：合并代码必须两人结对  
3：合并冲突，非自己的变动保持原样，和自己冲突的代码找相应的代码提交人确认如何解决冲突  
4：合并完成后，保证本地能编译能运行再 push  
5：合并到主干的代码必须通过测试，必须通过代码 review  
6：不同的功能从主干上拉新分支进行开发工作  
7：分支的命名需要加上，拉取人＋拉取说明  
8：上完线的分支要及时清理  

### <span id="head42">37 | 同时变更了文件名和文件内容如何处理？</span>

## <span id="head43"> 一个人改了文件名，一个人改了文件内容，还是可以自动处理的。</span>

前面章节讲 git 的文件存储时，说 git 存放 blob 文件时是以文件内容来区分的，并不以文件名来区分；此处的变更文件名操作和变更文件内容的操作能够自动被 git 处理，原因就在于 blob 文件并没有发生修改的冲突吧？如果其中一个人既变更了文件名又修改了文件，同时另一个人也修改了该文件的同一位置的内容，就会被 git 识别为冲突，而不能自动进行处理了。

### <span id="head44">38 | 把同一文件改成了不同的文件名如何处理？</span>

## <span id="head45"> 人为判断需保留哪一个文件。</span>

老师，你好。想问一下比较简单的多人协助开发代码怎么管理代码分支合并? 现在我作为一个小组长，每天要合并各个成员的代码，打包到测试、预上线等等环境。又涉及到出错回滚等等。每天都花挺多时间在这里。老师能否给个流程或者建议。谢谢了。  

作者回复: 你们看起来配置了专门的集成人员，你就充当了类似的角色。我补充说一下，如果你是懂业务并懂开发的，那么你来做这个涉及集成的一系列的工作，倒也挺好。否则就让开发自己来做集成。  
为了早点发现集成是否有冲突，或者集成是否能通过一些列的测试，你们团队可以考虑用工具帮你们尽快发现集成的问题。找一些持续集成的资料看看吧，可以借助 Jenkins 或 其他 CI 工具试试吧。  

# <span id="head46">第五章：Git 集成使用禁忌 (2 讲)</span>

### <span id="head47">39 | 禁止向集成分支执行 push -f 操作</span>

老师，如果发现之前提交的 commit 不想要了，想恢复成之前的样子，是不是就不得不用 git push -f 命令了呢？  

作者回复: 自己独自使用的分支，可以采用 push -f 的方式。  
团队集成分支，通常做法不是去掉不想要的 commit，而是把不想要的 commit 的内容采用 revert 的方式生成新的 commit，以此去掉不想要的变更。然后 push 到远端。  

### <span id="head48">40 | 禁止向集成分支执行变更历史的操作</span>

1：在主干分支上禁止使用 git push -f  
因为可能会抹掉其他的提交节点，假如有些东西提交了想回滚，那就修改后再提交  

2：在主干分支上禁止使用变更提交历史的命令  
因为会抹掉一些历史提交信息，我们貌似一直使用 rebase，主要是不喜欢混乱的提交线，不过也没出现什么问题，合代码出问题主要集中在合并冲突时，有些代码调整的存在问题。  

自己的分支随意，自己可以完全掌控，自己完全负责。公共分支是公地，不要做出影响他人的行为。  

# <span id="head49">第六章：初识 GitHub (6 讲)</span>

### <span id="head50">41 | GitHub 为什么会火？</span>

略

### <span id="head51">42 | GitHub 都有哪些核心功能？</span>

略

### <span id="head52">43 | 怎么快速淘到感兴趣的开源项目?</span>

之前在 github 上搜索项目, 直接用项目名搜索, 学习这一讲内容后, 以后可以添加其他限制条件, 如 stars:>1000,in:readme 等, 可以快速有效搜索自己刚兴趣的项目。

### <span id="head53">44 | 怎样在 GitHub 上搭建个人博客</span>

略

### <span id="head54">45 | 开源项目怎么保证代码质量？</span>

略

### <span id="head55">46 | 为何需要组织类型的仓库？</span>

老师，我有个问题，就是如果某用户加入了某个组织，这个组织可以管理 n 个仓库，那么我是这个组织的一员，是不是就可以对这些仓库进行操作？还是我加入了组织，还得加入到某个 team，才能对应进行操作？  
作者回复: 这个权限继承的方式，建议大家到 GitHub 平台上测试一下。平台的做法可能也会随时间而改变的。  

# <span id="head56">第七章：使用 GitHub 进行团队协作 (10 讲)</span>

### <span id="head57">47 | 创建团队的项目</span>

略

### <span id="head58">48 | 怎样选择适合自己团队的工作流？</span>

![](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855819.png)
![](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855676.png)

### <span id="head59">49 | 如何挑选合适的分支集成策略？</span>

![](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855678.png)

### <span id="head60">50 | 启用 issue 跟踪需求和任务</span>

github
![image.png](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855817.png)
gitlab
![](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855679.png)

### <span id="head61">51 | 如何用 project 管理 issue？</span>

github
![image.png](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855818.png)

### <span id="head62">52 | 项目内部怎么实施 code review？</span>

github:pull request
![image.png](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855684.png)

### <span id="head63">53 | 团队协作时如何做多分支的集成？</span>

略

### <span id="head64">54 | 怎样保证集成的质量？</span>

略

### <span id="head65">55 | 怎样把产品包发布到 GitHub 上？</span>

Travis－CI 工具

### <span id="head66">56 | 怎么给项目增加详细的指导文档？</span>

github 上面页面 wiki
![image.png](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855685.png)

# <span id="head67">第八章：GitLab 实践 (6 讲)</span>

### <span id="head68">57 | 国内互联网企业为什么喜欢 GitLab？</span>

略

### <span id="head69">58 | GitLab 有哪些核心的功能？</span>

![](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855769.png)

### <span id="head70">59 | GitLab 上怎么做项目管理？</span>

gitlab
![](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855797.png)

### <span id="head71">60 | GitLab 上怎么做 code review？</span>

gitlab:merge request
![](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855820.png)
![](https://xiaochen-pictures.oss-cn-guangzhou.aliyuncs.com/computer-pictures/1679235855821.png)

### <span id="head72">61 | GitLab 上怎么保证集成的质量？</span>

[CICD](https://so.csdn.net/so/search?q=CICD&spm=1001.2101.3001.7020)

### <span id="head73">62 | 怎么把应用部署到 AWS 上？</span>

CICD 的例子
