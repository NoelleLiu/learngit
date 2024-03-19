1. 版本控制：记录文件内容变化，以便将来查阅特定版本修订情况的系统。

   1. 迭代：本地版本控制系统 -》 集中化的版本控制系统 -〉分布式版本控制系统
   2. 分布式版本控制系统DVCS，distributed version control system，如Git

2. Git的三种状态：

   1. Committed 已提交，数据已经安全的保存在本地数据库中
   2. Modified 已修改，数据修改但没有存到数据库中
   3. Staged 已暂存，修改的文件被暂存到暂存区

   ![image-20240308105802373](/Users/liuxinyao/Library/Application Support/typora-user-images/image-20240308105802373.png)

3. Git工作流程：

   1. 在工作目录中修改文件
   2. 暂存文件，将文件的快照放入暂存区域
   3. 提交更新，将快照永久性存储到Git仓库目录

4. 初始化仓库

   1. git init
   2. git add
   3. git commit

5. 克隆现有仓库 - git clone url name   这里的name可以是自己给远程仓库重新起一个名字克隆到本地

6. Git文件的生命周期：

   ![image-20240308112635345](/Users/liuxinyao/Library/Application Support/typora-user-images/image-20240308112635345.png)

​	未跟踪的文件可能的情况：新创建、已存在未git add、未被包含到gitignore文件中（gitignore中文件的状态是已忽略）

7. 检查文件状态：git status，显示工作区、暂存区与本地版<strong>本地历史记录</strong>之间的差异
8. git add [file/folder]：将未追踪的文件开始追踪，也可以将追踪的文件的修改添加暂存区。 如果是文件夹就递归追踪目录下所有文件
9. 状态简单形式：git status --short / git status -s
   1. ？？未追踪
   2. A 新添加到暂存区
   3. 右M 修改了但没放到暂存区
   4. 左M 修改切放入了暂存区
10. 查看文件差异：git diff
    1. 无参数：git diff  查看修改后还没有暂存的起来的变化内容
    1. Staged: git diff --staged 查看已经暂存的将要添加到下次提交里的内容
11. 回顾提交历史： git log
    1. git log -p : 显示每次提交的内容差异。 （-p for patch)
    2. git log --stat：显示每次提交的简略的统计信息
    3. git log --pretty={format}: 用某种显示格式进行显示。     e.g. --pretty=oneline
12. 撤销修改操作：
    1. git commit --amend：订正最近一次commit提交并覆盖，并将当时暂存区修改提交
    2. git checkout -- file：取消在工作区的修改
    3. git reset file或者--soft/--hard/--mixed: 取消暂存区的修改以及仓库版本回退

13. 查看远程仓库：git remote [-v查看URL]
14. 从远程仓库获取数据：
    1. git fetch: 访问远程仓库，拉取还没有的数据
    2. Git pull: 







ref：1. 廖雪峰git：https://www.liaoxuefeng.com/wiki/896043488029600

2. Progit：https://www.progit.cn/#_git_basics_chapter
3. learningGitBranching：https://learngitbranching.js.org/?locale=zh_CN