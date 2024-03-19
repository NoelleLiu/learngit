Git-廖雪峰

1. git diff <file: 比较差异
   1. 无参数: 对比工作区与暂存区的差异
   2. git diff HEAD <file: 对比工作区与版本库的区别
   3. git diff --staged <file: 对比暂存区与版本库的区别
2. 版本回退
   1. git reset: 将本地仓库退/进到指定版本
   2. git log查看提交历史，查找回退版本的commit号
   3. git reflog查看历史命令，查看已经删除但想回的commit号
3. 撤销修改
   1. git checkout --file：丢弃工作区的修改
      1. 若文件只修改还没git add到暂存区，则回到最新版本库状态
      2. 若文件git add到暂存区还没有git commit提交，则回到暂存区的状态