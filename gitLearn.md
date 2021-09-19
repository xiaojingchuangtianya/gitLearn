# git 学习
> 完善自己的用户信息(使用了全局设置，单次设置后，后面不需要再设置了)  
 ` `
git config --global user.name "tester" 
git config --global user.email "tester@qq.com"
git config --global core.editor " 'E:\Microsoft VS Code\Code.exe' -multiInst -notabbar -nosession -noPlugin"
```
> 初始化一个本地仓库
git init

> 将本地的一些文件进行初始提交
git add *.py (添加到暂存区)
git commit -m "提交保存至git目录"

> 查看文件状态
git status
状态存在四种（未跟踪，未修改，修改，暂存）
    新建的文件是未跟踪的，通过git add 后为暂存
    直接通过git clone下来的整个完整文件夹都是未修改状态
    未修改状态的，被修改过后就是修改状态
    修改通过git add去到了暂存状态
    暂存区的通过git commit 后会转为未修改状态

> 从git将某个文件移除
git rm **.py

>将git的某个文件移动或者重命名
git mv a.py b.py

>查看每次进行提交时候执行的操作
git log 
参数具体有 
    -p 按每次补丁的形式输出差异，显示过程差异
    --stat 显示每次提交的统计信息，显示结果差异
    --name-only只输出改变文件的名字

>将git进行一次撤销操作
首先进行一次 git reset gitLearn.md,将文件从暂存区撤销
然后使用 git checkout -- gitLearn.md，将文件回退成未修改的时候

>查看远程的仓库
git remote -v 将远程仓库一一列举出来
git remote  add <name> <url>添加一个远程的Git仓库，指定一个简写名字给他


> 提交后如果发现有文件漏提交了，但又不希望新提交一次
git commit -m "第一次提交，未将所有应提交的commit"
git add next.py 将希望补上一起提交的add
git commit --amend 这一次的提交会将上一次的进行覆盖合并一起上传

