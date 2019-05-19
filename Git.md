## Git



> [廖雪峰Git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)



- 配置Git
  - **``$ git config --global user.name "Your Name"``**
    **``$ git config --global user.email "email@example.com"``**
  - 初始化**`$ git init`**
  - 显示颜色**`git config --global color.ui true`**
  - 配置别名**`$ git config —global alias.st status`**(设置status别名st)

- 基本操作

|         操作         | 命令                                                         |
| :------------------: | ------------------------------------------------------------ |
|         添加         | **```$ git add <file>```**                                   |
|         提交         | **```$ git commit - m <"message">```**                       |
|       查看状态       | **```$ git status```**                                       |
|       查看修改       | **```$ git diff <file>```**                                  |
|       历史提交       | **```$ git log```**<br /><!---pretty=oneline : 简略版-->     |
|       历史命令       | **```$ git reflog```**                                       |
|       版本穿梭       | $ git reset —hard <commit-id>`**<br /><!---hard : HEAD^(回退上一个版本) / id--> |
|   撤销修改(工作区)   | **`$ git checkout — <file>`**<br /><!--用于还没add到暂存区时恢复到版本库一模一样的状态--> |
|   撤销修改(暂存区)   | **`$ git reset HEAD <file>`**<br /><!--用于已经add到暂存区的修改撤销掉，重新放回工作区--> |
|     删除(暂存区)     | **`$ git rm <file>`**                                        |
|     关联远程仓库     | **`$ git remote add <origin name> <address> `**              |
|       取消关联       | **`$ git remote rm <origin name>`**                          |
|    推送到远程仓库    | **`$ git push origin master`**                               |
|       创建分支       | **`$ git branch "branch name"`**                             |
|       切换分支       | **`$ git checkout "branch name"`**                           |
|    创建并切换分支    | **`$ git checkout -b "branch name"`**                        |
|       查看分支       | **`$ git branch`**                                           |
| 合并某分支到当前分支 | **`$ git merge <branch name>`**                              |
|       删除分支       | <!--d : 合并后删除--><br /><!---D : 未合并强行删除-->        |
|     保存工作现场     | **`$ git stash`**                                            |
|     恢复工作现场     | **`$ git stash pop`**                                        |
|       打上标签       | **`$ git tag <tag name>`**<br /><!--默认打在HEAD上,也可以值指定一个commit id--><br /><!--例如：git tag v1.0 c1321abf20db--> |
|     带信息的标签     | **`$ git tag -a <tag name> -m "message"`**                   |
|     查看所有标签     | **`$ git tag`**                                              |
|     查看某个标签     | **`$ git show <tag name>`**                                  |
|       删除标签       | **`$ git tag -d <tag name>`**                                |
|    推送标签到远程    | **`$ git push origin <tag name> `**                          |
|  推送所有标签到远程  | **`$ git push origin --tags`**                               |
|     删除远程标签     | **`$ git push origin :refs/tags/<tag name>`**                |

- 当分支合并起冲突时，需要手动解决冲突再提交。