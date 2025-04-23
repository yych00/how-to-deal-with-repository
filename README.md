# 如何上传单个文件到分支
单个文件：temp.txt

仓库地址：https://github.com/yych00/how-to-deal-with-repository.git

目标分支：branch-1

## 本地目录
    cd .docx catalog

## 初始化 Git 仓库
    git init
返回值：Reinitialized existing Git repository in E:/$$$$$$/.git/
  
## 添加远程仓库（指向 GitHub 上的仓库地址）
    git remote add origin https://github.com/yych00/$$$$$$.git
返回值：error: remote origin already exists.

## 创建并切换到目标分支 branch-1
    git checkout -b branch-1
返回值：fatal: a branch named 'branch-1' already exists

## 添加 temp.txt 文件
    git add temp.txt

## 提交这些变更到本地仓库，写一条提交信息
    git commit -m "Add temp.txt"
返回值：
返回说明：

## 把本地 main 分支推送到远程仓库的 branch-1 分支
    git push -u origin branch-1


