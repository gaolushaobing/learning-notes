# Tools(工具)

---

## command line 命令行

---

### basic-commmand 基础命令

> 以后如无特殊表示, 命令行均用 Cmder工具

```shell
# pwd (point working directory 指向工作目录)
$ pwd

# ls (List information about the FILEs 列出当下文件)
$ ls
$ ls -l  # long information 详细信息
$ ls -la # 长格式 all 文件
$ ls -lh #把字节大小转换为B M
$ ls -lt #默认修改的时间time排序
$ ls -ltr #revers 倒过来时间修改排序
$ ls -R 文件名 # 递归方式显示文件名下的所有子目录信息

# tree 树型显示目录
$ tree dir_name

# 清屏
$ clear

# cd (change directory)
$ cd directoryName
$ cd ../ # 上一级
$ cd ~ # 主目录 (cmder无  )

# mkdir (make directory 创建目录文件夹)
$ mkdir directoryName 
$ mkdir project\app\css # 自动创建补充其父目录

# mv (move 移动)
$ mv test\01\001 test\02\ # mv 要移动的文件 要移动到的位置
$ mv -v test\01\001 test\02\ # 显示结果信息
$ mv cess.txt hello.txt # 重命名文件名

# touch 创建触摸初始化文件
$ touch ts.txt
$ touch file-{01..10}.txt # 批量创建文件

# rm 删除
$ rm *.txt

# cp copy复制
$ 

# expLorer 探险,探索,资源管理器, -连字符 _属性
$ explorer # 打开资源管理器
$ explorer G:\learn_note\test # 在资源管理器中打开文件夹
$ explorer .git #在资源管理器中打开当前目录下的这个文件夹
```

---

## git (分布式版本控制系统)

Linux之父Linus在02年花了两周写了Git, 成为了流行的分布式版本控制系统, 08年Github上线后免费提供git存储, 几乎一统江湖, 目前所有人的共识是git是最好用的, 且开源.

集中式的工作方式是联网, 从服务商下载, 干完活把作品推过去
分布式的不但可以互相推送, 也可以用其中一个作为服务器(交换中心)推送

CVS是最早且开源的集中式, 提交问题较多, SVN也是开源的集中式, 目前用的最多,修复了前者一些问题

```shell
$ ssh-keygen -t rsa -C "gaolushaobing@gmail.com" # 生成SSH 
```

然后在用户主目录里找到`.ssh`目录，里面有`id_rsa`和`id_rsa.pub`两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公共, 提交在Git仓库




![](./images/gitindex.jpg)

git的大部分工作是把文件在工作区,暂存区和版本库中移来移去, 例如`git add`是把文件从工作区复制到暂存区, `git commit`又把文件从暂存区复制/提交到版本库

> 暂存去的概念优点类似于 选择商品 -> 购物车 -> 结账 中 购物车的概念, 可以多次选择多次提交,并且可以多次改变处理悔改后再提交
> **暂存区**的设计也是和SVN的一大区别



### help 帮助信息

```shell
$ git help # 查看帮助信息, 有一些常用的指令和解释
$ git help -a # 查看所有命令
$ git help -g # 简单的使用手册目录 attributes everyday etc.
$ git help attributes #弹出本地html页面显示attributes详细内容
$ git help add #弹出本地页显示add指令文档 
$ git clone # 克隆地址
```

> 目前版本的git是新弹出html页面, 之前文档信息显示在控制台, 翻页B 退出Q

---

### config 配置信息

安装了git以后一般是要配置下, 作者, 邮箱, 浏览器等等; 可以使用 `$ git help config` 指令查看详细文档, 只不过文档太长了.

配置有三种范围, 首先是`系统范围`, 不论哪个用户登录, Git都会用这个系统范围的配置, 针对计算机登录用户的范围是`global(全局范围)`,大部分是用此配置, 此外还有`项目范围`

```shell
$ git config --global user.name 'Kevin' # 配置用户名
$ git config --list # 查看配置信息
$ git config --unset --global user.name # 重置 
$ git config --global user.email 'gaolushaobing@gmail.com' 
$ git config --global color.ui true # 彩色显示git
$ cat ~/.gitconfig # 查看根目录下的配置文件
```

---

### init (initialize 初始)

若用git控制项目, 首先是要先初始化, 初始的是一个空的版本库 

git会把创建和需要的文件都放在生成的`.git`文件里, 有了它以后, git就会跟踪和监听这个`.git`所在目录的文件的变化, 这样就git就可以进行版本控制

`.git`文件里面一般不需要手动操作, 如果不想跟中目录, 可以删除`.git`文件夹

```shell
# 首先创建一个文件夹
$ mkdir movietalk
movietalk/$ git init # 初始化一个空的 .git 文件
```

---

### commit (提交) 流程

一个提交的流程: 项目修改变动 => 告诉git要提交修改的哪些文件 => 确认提交 => 提交时添加描述信息

```shell
# 查看状态
$ git status # 查看目前状态
  -> On branch master # 当天所在分支是 master(主分支'控制 主要 大师')
  -> No commits yet # 还没有提交

# 新建/修改文件后(在工作区内)
$ git status
  -> Untracked files: # 此时会显示未被跟踪(暂存)的文件

# 添加到暂存区
$ git add index.html # 添加要跟踪的文件到暂存, 添加所有文件是 git add .

$ git status
  -> Changes to be committed: # 主分支上尚未提交, 要提交的更改的信息:

# 提交到版本库
$ git commit -m '添加index.html文件' #cmder貌似不能有空格

# 再次查看
$ git status # 没有可提交的 工作目录是干净的

# 查看以往提交 查看提交日志(版本库日志)
$ git log
  commit a78fec5191f9fd1e99193421b234432d268d6d10 (HEAD -> master)
  Author: Kevin <gaolushaobing@gmail.com>
  Date:   Fri Aug 3 15:33:51 2018 +0800
    // 提交信息
```

---

### diff different 

diff比较的是暂存区与工作区之间的不同,

```shell
# 修改文件后查看文件状态 (tools.md)
$ git status # modified修改的文件 还未暂存
$ git diff tools.md # 查看修改前后的区别, 加文件就是该文件明细, 不加就是所有
$ git add 01_tools/tools.md
$ git diff --staged ## 查看暂存区和版本库之间的区别
```

---

### rename 重命名

```shell
# 在编辑器里重命名文件后, 会提示删除了一个文件, 然后新增了未跟踪文件
$ git status
$ git rm style.css
$ git add theme.css
```

---

### mv 重命名或者移动

```shell
$ git mv theme.css tongyaojia.css
# 修改名字会在暂存区, 可以直接提交修改
# git不跟踪文件夹, 除非此文件夹包含文件, 也就是说git不会跟踪空白目录
# 可以创建文件夹然后移动文件
$ git mv tongyaojia.css 01_tools/css
$ git mv tongyaojia.css 01_tools/css
```

---

### rm remove 删除Git中跟踪的文件

既可以在文件系统中把文件删除, 再用rm命令把文件从git目录中删除掉, 还可以直接用git的rm命令删除文件, 删除多个用空格把不用的文件名字隔开, 如果要删除整个目录,包括目录里面的文件,可以加上一个`-r`的参数,表示递归, 

```shell
$ git rm -r css/
$ git rm index.html
# 执行后直接就是在暂存区有
    Changes to be committed:
      (use "git reset HEAD <file>..." to unstage)

            deleted:    css/tongyaojia.css
            deleted:    index.html
$ git commit -m 'delete file'
```

使用`rm`指令之前, 要确定这个文件已经被追踪了. 并且没有将要提交的修改, 如果修改后还没有提交, git是无法进行删除的, 需要先`add` 添加修改,然后提交以后再删除, 


---

### HEAD (头部,log头部,暗指最近的操作 checkout'检测'的意思)
`rm` 删除后,在暂存区显示deleted:xxxx 如果这个时候还没有提交, 想要改变主意的话

```shell
# 从暂存区回复到工作区
$  git checkout HEAD -- index.html

# 恢复删除并提交过的文件
# 需要恢复到上一次提交的状态
$ git checkout HEAD^ # 这表示最近的上一次提交 两个^^就是上两次提交
```

---

### revert恢复到某一个提交

```shell
$ git revert 分支号
```

---

### reset

默认提交以后, 头部的指针就指向最后一次的提交, reset可以切换指针,然后下一次提交,就会覆盖掉之后的所有提交. 

- `--soft` 是软重置 ,这个不会替换工作区和暂存区,
- `--hard` 会直接重置工作区和暂存区
- `--mixed` 默认项, 会把暂存区恢复到指定的状态 并且把指针指向这个提交

---

### branch 分支

想要为项目添加新的特性, 但又不确定是否可行, 或者修改项目bug的时候, 可以给项目创建一个分支, 在分支上面对项目提交一些修改, 完成以后可以把分支合并到一起,查看当前所在的分支

- `git status` on branch master (在主分支上)
- `git branch` 查看项目所有分支

创建分支还是使用`git branch` 后面跟分支名称, 分支的内容如果可就合并,如果不可以就删除

要想用分支修改需要先切换分支, `git checkout 分支名称` 

---

### checkout

切换到分支以后, 对项目的修改只会在分支的情况下有效, 修改文件后, 缓存提交,使用`git log --oneline`查看分支的提交.

可以再切回 `master` 分支 `$ git checkout master`( **切换分支** )

`$ git log --oneline --all (可选显示的数量-n) (可选图标 --graph)` **可以查看所以分支的提交**.


---

### branch diff 查看分支的区别

`$ git diff master..其他分支名称 (可选:对比文件名称)` 可以查看分支之间的区别

---

### fast-forward

如果我们在分支的提交也想应用到主分支, 先查看当前分支`git branch` 然后切换到 主分支

`$ git merge 要合并的分支名称`  因为master没有做新的提交, 所以合并模式是fast-forward.

---

### merge 合并

如果创建分支后, 分支进行了提交, 而切回master后, 也进行了提交, 这个时候, master与分支刚开始创建的时候不一样, 这个时候的合并其实就是真正的提交, 而这个提交有时候会遇到冲突, 这个时候就需要去解决冲突以后再合并, 

> 如果想快速进行暂存和提交可以使用一个快捷方式 ` $git commit -am '描述信息'`

```shell
# 先用图表查看一下目前分支的区别
$ git log --oneline --all -3 --graph
```

`$ git merge 分支名称` 然后合并提交
---

### conflict (冲突, 矛盾 手工解决)

使用`abort` 就是放弃合并 本身单词是流产, 终止计划等等,如果有冲突就在编辑器里进行选择,然后进行提交,`git add .`  然后在 `git commit` 不需要穿参数

```shell
$ git log --oneline --all -10 --graph
```

---

### rm 删除/重命名分支

```shell
# 加 -m 参数, 然后输入旧名字和新名字, 中间用空格隔开
$ git branch -m bugfix newbugfix 

# 加-d 后跟分支名称就是删除分支 多条用空格隔开
$ git branch -d dele dele-rest
```

---

### stash (藏匿 存储)

stash可以暂时把修改保存到一个地方, 然后继续修改其他地方,等需要用到这个修改的时候再拿出来

`$ git stash save '描述信息'`

执行完该指令以后, 使用 `$ git status` 是查看不到状态的, 想要查看已经的贮藏, 需要用到`$ git stash list` 来查看

如果想要对不一下区别, 就是使用: `$ git stash show -p stash@{0}`  *-p是以补丁的方式*

如果要应用到工作进度: `$ git stash apply stash@{0}`

如果想要删除就使用:  `$ git stash drop stash@{0}`

---

### log 日志

> 进入长文模式的时候 使用 **F** 键可以进行翻页, 使用 **B** 键是进行向上翻页, 按下 **Q** 是退出当前显示

```shell
$ git log # 默认显示的详细的提交记录, 做着 信息 ID号
$ git log --oneline #单行显示
$ git log --oneline -5 # 控制输出的行数
$ git log --oneline -5 --author='gaolushaobing' #筛选作者
$ git log --oneline --grep='index.html' # 搜索的方式
$ git log --oneline --before='2018-08-05' # 指定某时间之前的提交
$ git log --oneline --before='1 week' # 一周前
$ git log --oneline --before='2 days' # 两天前
$ git log --oneline --graph # 加入图形效果
$ git help log # 可以查看关于log的更多文档, 就是有点长, 太长了.
```

---

### alias 别名, 给经常用的指令添加别名(快捷名字)

使用alias 可以简化输入的指令, 设置别名用的是 `git config --global alias.co checkout`

保存的别名配置会保存在 `.gitconfig` 文件内 可以使用 `$ cat ~/.gitconfig` 来查看

---

### ignore 驳回诉讼 忽略的文件

如果有不想让git跟踪的文件, 可以在全局设置里面设置

```shell
$ git config --global core.excludesfile ~/.gitignore_global
$ vim ~/.gitignore_global # 输入要忽略的文件名
```

另外忽略的文件可以参考[gist.github.com/octocat/9257657](gist.github.com/octocat/9257657)

---

### gitignore 为每个项目创建忽略的列表

```shell
# 先进入到项目的根目录, 然后用vim创建
$ vim .gitignore
*.log
```

他不会已经跟踪的文件, 可以先rm删除.

此外还可以参考模版: [github.com/github/gitignore](github.com/github/gitignore)

---

### remote (远程) 

我们可以把本地的项目推送到远程仓库,

---

### origin (源点 开端)

在github上创建好项目后 ->

```shell
# 本地新建
touch README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://xxxxxx.git
git push -u origin master
```

```shell
# 本地已有的项目推送
git remote add origin https://......xxx.git
git push -u origin master
```

```shell
git remote #查看远程 fetch (提取)
git remote -v # 查看详细信息
git remote -rm 名称 # 移除远程
```

---

### push 本地推送到远程

`-u` 参数意思是跟踪远程分支的变化

- `$ git push -u origin master` 第一次要输入用户名和密码

```shell
$ git branch -a # 查看所有分支
$ git branch -r # 查看远程分支
```

---

### remote-workflow 使用远程版本库流程

- download 单纯的下载项目代码
- git clone 如果需要项目的版本库就使用该指令, 可以查看项目所有的提交
- fork 到自己的账户下面, 再clone到自己本地, 然后自己开发 
- pull request 向远程提交自己的修改, 对方可以拒绝或采纳
- contributors 成为项目的贡献者, 需要所有者添加

### clone 

- `git clone https://github.com/xxxx/xxx.git (可选,自己命名的目录名称)` 把项目克隆到本地

---

### fetch 提取

克隆到本地后, 远程版本库又有了新的提交, 此时可以用到fetch

刚开始使用 `git status` 会提示 `On branch master, Your branch is up-to-date with 'origin/master'. nothing to commit, working dirctory clean` 没有可用的更新, 此时需要提取一下最新的提交.

输入`git fetch` 会提示已经提取了更新, 并且放在了本地的` origin/master`分支上面, 此时可以使用 `git merge origin/master`进行合并分支.

---

### fork (叉子, 分叉)

如果自己想开发版本可以点击`fork` 到自己的账户下面, 然后再 `clone`到自己的本地上进行开发,

> 项目的根目录的README.md 文件会自动在根目录下, 并且github会自动的把其编译成HTML的格式, 放在项目的页面下方.

---

### pull requests (合并请求) 

如果想为不是自己所有的远程版本库进行提交, 且自己不是项目的贡献者的话, 可以做一个`pull requests`  **(合并请求)** 所有者收到这个信息的话, 他们可以选择是否合并.

- 在自己的项目中, 点击`pull requests`后 再点击 `New Pull requests` 
- 依据自己和远程版本的区别进行编辑,然后添加标题和描述,然后点击发送

作为远程项目拥有者, 可以在版本旁边看到Pull Requests 的请求, 点击发来的请求中的`Commits` , `Files changed`中可以查看发生变化的文件, 如果选择接受, 可以合并. 

---

### collaborator (合作者, 项目贡献者) 

如果想要多人合作一个项目, 

- 添加用户到项目的贡献者列表, `Settings` -> `Collaborator` -> 

### git desktop (git桌面应用工具)

- 登录
- 添加本地版本库
- `History` 可以查看历史提交记录
- `Repository settings` 可以设置远程版本库的地址以及忽略跟踪的文件.

---

### tag 项目标签

不同的标签指向不同时期的提交

- git tag
- git tag v1.0.1
- git show v1.0.1
- git tag -a v1.0.2 -m '注释'

最后使用`git checkout tag名/分支名 来切换.

- `git tag -a tagName 对应的提交ID` 绑定tag名字
- `git tag -d tagName` 删除标签
- `git push --tags` 推送本地所有标签





















