# git 学习
> 完善自己的用户信息(使用了全局设置，单次设置后，后面不需要再设置了)  
 ` `
git config --global user.name "tester" 
git config --global user.email "tester@qq.com"
git config --global core.editor " 'E:\Microsoft VS Code\Code.exe' -multiInst -notabbar -nosession -noPlugin"
```


>从git将某个文件移除，不是删除
git rm **.py

>将git的某个文件移动或者重命名
git mv a.py b.py

>查看每次进行提交时候执行的操作
git log 
参数具体有 
    -p 按每次补丁的形式输出差异，显示过程差异
    --stat 显示每次提交的统计信息，显示结果差异
    --name-only只输出改变文件的名字
