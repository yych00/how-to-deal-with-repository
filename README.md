# 如何管理仓库
Learn to upload code and manage the repository.

有多个分支可以查看！

### 1.cd到目录
    cd <CMakeList.txt catalog>

### 2.初始化 Git 仓库
    git init
重复建仓返回值：Reinitialized existing Git repository in E:/$$$$$$/.git/
  
### 3.添加远程仓库（指向 GitHub 上的仓库地址）
    git remote add origin <https://github.com/...>
    
    git remote add origin https://github.com/yych00/how-to-deal-with-repository.git
重复添加返回值：error: remote origin already exists. 

表明仓库已经存在

如果已添加过，可删除：

    git remote remove origin

### 4. 拉取远程 main 分支，避免推送冲突
    git fetch origin
    
    git checkout -B main origin/main

### 5.把当前目录下的文件除了.gitignore都加入 Git 的暂存区
    git add .
或者添加单个文件

    git add temp.txt
    
### 6.提交这些变更到本地仓库，写一条提交信息
    git commit -m "This is a commit message"
重复提交返回值：

On branch main

nothing to commit, working tree clean

返回说明：

•  所有的更改已经被提交到了本地仓库

•  当前文件夹里的文件也没有再做任何修改

•  所以 Git 认为：“没有新的变动可提交”

### 7.把当前分支改名为 main（Git 默认以前是 master，现在都用 main）
    git branch -M main

### 8.把本地 main 分支推送到远程仓库的 main 分支，并建立跟踪关系
    git push origin main

    git push -u origin main

    情况	                        推荐做法
    远程仓库是空的                   git push -u origin main
    远程仓库有内容，但你要合并	git pull origin main --allow-unrelated-histories
    远程仓库内容不需要保留            git push -f origin main



